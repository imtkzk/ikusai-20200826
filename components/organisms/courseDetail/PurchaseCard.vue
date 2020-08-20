<template>
    <div class="detail-apply" :class="{ 'nodisplay': scrollY > 1400 }">
      <div class="detail-apply-box">
        <div class="detail-apply-image">
          <div><img src="~/assets/img/detail/view.jpg" class="img--fit" alt="preview"></div>
          <div class="detail-apply-play">
            <div class="detail-apply-mark"></div>
            <p>このコースをプレビュー</p>
          </div>
        </div>
        <div class="detail-apply-content">
          <div id="floathing" class="detail-apply-prices">
            <div class="detail-apply-price">
              <p>¥100,000</p>
              <p>業界最安値！</p>
            </div>
            <div id="payment-open" class="detail-buy-btn">
              <SendForm>今すぐ購入</SendForm>
            </div>
          </div>
          <ul class="detail-course-tags">
            <li class="detail-course-tags--video">24 videos</li>
            <li class="detail-course-tags--time">200 hrs</li>
            <li class="detail-course-tags--tag">機械学習、Webアプリ</li>
          </ul>
          <div class="detail-share">
            <p>このコースをSNSでシェアする</p>
            <div class="detail-social">
              <a href="#"><img src="~/assets/img/common/facebook_b.png" class="img--fit" alt="Facebook"></a>
              <a href="#"><img src="~/assets/img/common/twitter_b.png" class="img--fit" alt="twitter"></a>
            </div>
          </div>
        </div>
      </div>
      <div class="detail-apply-btn">
        <p class="detail-apply-accent">動画見放題キャンペーンで<span>50</span>万円お得</p>
        <SendForm>キャンペーンの詳細を確認する</SendForm>
      </div>
      <PayApply />
    </div>
</template>

<script>
    import SendForm from '~/components/atoms/buttons/SendForm.vue'
    import PayApply from '~/components/organisms/common/PayApply.vue'

export default {
        components: {
            SendForm,
            PayApply
        },   
        data() {
    return {
      // 座標を指定
      scrollY: 0
    }
  },
  mounted() {
    window.addEventListener('scroll', this.handleScroll)
  },
  methods: {
    handleScroll() {
      this.scrollY = window.scrollY
    }
  }
}
</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
/* ---------------------------------- detail-apply  */

.detail-apply {
  position: relative;
  top: vw-sp(-60);
  margin: 0 auto vw-sp(80) auto;
  width: vw-sp(620);
}

.detail-apply-image {
  position: relative;
  img {
    border-radius: vw-sp(15) vw-sp(15) 0 0;
  }
}

.detail-apply-play {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  p {
    margin-top: 1em;
    color: rgb(255,158,0);
    font-weight: 700;
    text-align: center;
    white-space: nowrap;
    text-shadow:
    2px  2px 1px #ffffff,
    -2px  2px 1px #ffffff,
    2px -2px 1px #ffffff,
    -2px -2px 1px #ffffff,
    2px  0px 1px #ffffff,
    0px  2px 1px #ffffff,
    -2px  0px 1px #ffffff,
    0px -2px 1px #ffffff;
  }
}

.detail-apply-mark {
  position: relative;
  display: block;
  margin: 0 auto;
  width: vw-sp(150);
  height: vw-sp(150);
  background-image: -moz-linear-gradient( 0deg, rgb(255,158,0) 0%, rgb(255,181,23) 100%);
  background-image: -webkit-linear-gradient( 0deg, rgb(255,158,0) 0%, rgb(255,181,23) 100%);
  border-radius: 50%;
  border: vw-sp(4) solid $color-base;
}

.detail-apply-mark:before {
  content: '▶︎';
  position: absolute;
  top: 50%;
  left: 50%;
  margin-left: .1em;
  color: $color-base;
  font-size: vw-sp(38);
  font-weight: 700;
  transform: translate(-50%, -50%);
}

.detail-apply-box {
  margin-bottom: vw-sp(100);
  background-color: $color-base;
  border: vw-sp(3) solid $color-text;
  border-radius: vw-sp(15);
}

.detail-apply-content {
  border-top: vw-sp(3) solid $color-text;
  padding: vw-sp(40) vw-sp(50) vw-sp(35) vw-sp(50);
}

.detail-apply-price {
  display: flex;
  justify-content: center;
  align-items: center;
}

.detail-apply-price p:nth-child(1){
  font-family: $font2;
  font-size: vw-sp(42);
  font-weight: 700;
}

.detail-apply-price p:nth-child(2){
  margin-left: 1em;
  font-size: vw-sp(23);
  font-weight: 700;
}

.detail-buy-btn {
  margin: vw-sp(22) 0 vw-sp(25) 0;
    font-size: vw-sp(30);
}

.detail-buy-btn .cmn-btn {
  border: none !important;
  p {
    font-size: vw-sp(30);
  }
}

.detail-share {
  padding-top: vw-sp(30);
  border-top: vw-sp(3) solid $color-text;
  p {
    margin-bottom: 1em;
    font-size: vw-sp(23);
    font-weight: 700;
    text-align: center;
    line-height: 1.4em;
  }
}

.detail-social {
  display: flex;
  justify-content: center;
  align-items: center;
}

.detail-social a {
  display: block;
  margin-right: vw-sp(30);
  width: vw-sp(41);
}

.detail-social a:last-child {
  margin-right: 0;
}

.detail-social a:hover {
  opacity: 0.7;
}


@media screen and (max-width: $breakpoint1-max) {

  .detail-apply-prices.is-fixed {
    position: fixed;
    bottom: 0;
    left: 50%;
    padding: vw-sp(35) vw-sp(60) vw-sp(30) vw-sp(60);
    background-color: $color-base;
    width: 100%;
    transform: translateX(-50%);
    z-index: 10;
  }

  .detail-apply-prices.is-fixed .detail-buy-btn {
    margin: vw-sp(20) auto 0 auto;
    width: vw-sp(500);
  }
}

@media screen and (min-width: $breakpoint1) {

  .detail-apply {
    position: fixed;
    top: vw-pc(145);
    left: 50%;
    margin: 0 0 0 vw-pc(240);
    width: vw-pc(360);
    z-index: 3;
  }
@keyframes show{
    from{
        opacity: 0;
    }
    to{
        opacity: 1;
    }
}
.nodisplay {
  opacity: 0;
  transition: opacity .3s linear 0s;
}
  .detail-apply-image {
    img {
      border-radius: vw-pc(10) vw-pc(10) 0 0;
    }
  }

  .detail-apply-mark {
    width: vw-pc(100);
    height: vw-pc(100);
    border: vw-pc(3) solid $color-base;
  }

  .detail-apply-mark:before {
    font-size: vw-pc(28);
  }

  .detail-apply-box {
    margin-bottom: vw-pc(55);
    border: vw-pc(2) solid $color-text;
    border-radius: vw-pc(10);
  }

  .detail-apply-content {
    border-top: vw-pc(2) solid $color-text;
    padding: vw-pc(40) vw-pc(30) vw-pc(35) vw-pc(30);
  }

  .detail-apply-price p:nth-child(1){
    font-size: vw-pc(28);
  }

  .detail-apply-price p:nth-child(2){
    font-size: vw-pc(13);
  }

  .detail-buy-btn {
    margin: vw-pc(12) 0 vw-pc(15) 0;
      font-size: vw-pc(20);
  }

  .detail-buy-btn .cmn-btn {
    p {
      font-size: vw-pc(20);
    }
  }

  .detail-share {
    padding-top: vw-pc(20);
    border-top: vw-pc(2) solid $color-text;
    p {
      font-size: vw-pc(13);
    }
  }

  .detail-social a {
    margin-right: vw-pc(20);
    width: vw-pc(31);
  }
}

@media screen and (min-width: $breakpoint2) {

  .detail-apply {
    position: fixed;
    top: 145px;
    left: 50%;
    margin: 0 0 0 240px;
    width: 360px;
  }

  .detail-apply-image {
    img {
      border-radius: 10px 10px 0 0;
    }
  }

  .detail-apply-mark {
    width: 100px;
    height: 100px;
    border: 3px solid $color-base;
  }

  .detail-apply-mark:before {
    font-size: 28px; font-size: 2.8rem;
  }

  .detail-apply-box {
    margin-bottom: 55px;
    border: 2px solid $color-text;
    border-radius: 10px;
  }

  .detail-apply-content {
    border-top: 2px solid $color-text;
    padding: 40px 30px 35px 30px;
  }

  .detail-apply-price p:nth-child(1){
    font-size: 28px; font-size: 2.8rem;
  }

  .detail-apply-price p:nth-child(2){
    font-size: 13px; font-size: 1.3rem;
  }

  .detail-buy-btn {
    margin: 12px 0 15px 0;
      font-size: 20px; font-size: 2.0rem;
  }

  .detail-buy-btn .cmn-btn {
    p {
      font-size: 20px; font-size: 2.0rem;
    }
  }

  .detail-share {
    padding-top: 20px;
    border-top: 2px solid $color-text;
    p {
      font-size: 13px; font-size: 1.3rem;
    }
  }

  .detail-social a {
    margin-right: 20px;
    width: 31px;
  }
}

/* ---------------------------------- detail-apply-btn  */

.detail-apply-btn {
  position: relative;
}

.detail-apply-accent {
  position: absolute;
  top: vw-sp(-50);
  left: 50%;
  display: inline-block;
  font-family: $font2,$font1;
  font-size: vw-sp(24);
  font-weight: 700;
  white-space: nowrap;
  -webkit-transform: translateX(-50%);
  transform: translateX(-50%);
  > span {
    margin: 0 .05em;
    font-size: 1.5em;
  }
}

.detail-apply-accent:before,
.detail-apply-accent:after {
  content: '';
  position: absolute;
  top: 50%;
  display: inline-block;
  width: vw-sp(20);
  height: vw-sp(28);
  background-size: contain;
  background-repeat: no-repeat;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
}

.detail-apply-accent:before {
  left: -1.5em;
  background-image: url(~assets/img/common/accent-l.png);
}

.detail-apply-accent:after {
  right: -1.5em;
  background-image: url(~assets/img/common/accent-r.png);
}

@media screen and (min-width: $breakpoint1) {

  .detail-apply-accent {
    top: vw-pc(-30);
    font-size: vw-pc(14);
  }

  .detail-apply-accent:before,
  .detail-apply-accent:after {
    width: vw-pc(10);
    height: vw-pc(14);
  }
}

@media screen and (min-width: $breakpoint2) {

  .detail-apply-accent {
    top: -30px;
    font-size: 14px; font-size: 1.4rem;
  }

  .detail-apply-accent:before,
  .detail-apply-accent:after {
    width: 10px;
    height: 14px;
  }
}


.detail-course-tags {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  margin-bottom: vw-sp(60);
}

.detail-course-tags li {
  position: relative;
  padding: .3em .5em .3em vw-sp(55);
  font-family: $font2,$font1;
  font-size: vw-sp(23);
  font-weight: 700;
  line-height: 1.6em;
}

.detail-course-tags li:before {
  content: '';
  position: absolute;
  top: .4em;
  left: .6em;
  display: inline-block;
  width: vw-sp(27);
  height: vw-sp(27);
  background-size: contain;
  background-repeat: no-repeat;
}

.detail-course-tags--video:before {
  background-image: url(~assets/img/course/video.png);
}

.detail-course-tags--time:before {
  background-image: url(~assets/img/course/time.png);
}

.detail-course-tags--tag:before {
  background-image: url(~assets/img/course/tag.png);
}

.detail-course-tags li:last-child {
  border-bottom: none;
}

@media screen and (min-width: $breakpoint1) {

  .detail-course-tags {
    margin-bottom: vw-pc(40);
  }

  .detail-course-tags li {
    padding: .3em .5em .3em vw-pc(35);
    font-size: vw-pc(13);
  }

  .detail-course-tags li:before {
    width: vw-pc(17);
    height: vw-pc(17);
  }
}

@media screen and (min-width: $breakpoint2) {

  .detail-course-tags {
    margin-bottom: 40px;
  }

  .detail-course-tags li {
    padding: .3em .5em .3em 35px;
    font-size: 13px; font-size: 1.3rem;
  }

  .detail-course-tags li:before {
    width: 17px;
    height: 17px;
  }
}

</style>
