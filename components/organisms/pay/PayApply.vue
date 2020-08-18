<template>
    <section class="sec sec--pay-apply">
      <div class="sec__in">
        <div class="apply-form">
          <div class="apply-form-box">
            <ul class="form-step">
              <li><p>STEP<br>01</p></li>
              <li class="is-active"><p>STEP<br>02</p></li>
              <li><p>STEP<br>03</p></li>
            </ul>
            <h3 class="apply-form-head">基本情報の入力</h3>
            <div class="apply-form-box__in">
              <InputText type="text" placeholder="例）田中">名字</InputText>
              <InputText type="text" placeholder="例）太郎">名前</InputText>
              <InputText type="email" placeholder="例）田中">メールアドレス</InputText>
              <InputText type="tel" placeholder="例）070-1234-1234">電話番号</InputText>
              <InputText type="text" placeholder="例）111-2222">郵便番号</InputText>
              <InputText type="text" placeholder="例）東京都">都道府県</InputText>
              <InputText type="text" placeholder="例）千代田区">市区町村</InputText>
              <InputText type="text" placeholder="例）神田紺屋町15">番地</InputText>
            </div>
            <p class="apply-step2-desc">住所情報は請求書の郵送を希望される際に使用いたします。</p>
          </div>
          <div class="apply-form-box">
            <ul class="form-step">
              <li><p>STEP<br>01</p></li>
              <li><p>STEP<br>02</p></li>
              <li class="is-active"><p>STEP<br>03</p></li>
            </ul>
            <div>
              <h3 class="apply-form-head">申し込み内容の確認</h3>
              <div class="apply-step3">
                <div class="apply-step3-top">
                  <h4 class="apply-step3-head">お申し込みコース</h4>
                  <div class="apply-step3-detail">
                    <h5 class="apply-step3-detail-head">ディープラーニングハンズオンコース</h5>
                    <dl class="apply-step3-prices">
                      <dt><span>消費税（10%）</span></dt>
                      <dd>¥100,000</dd>
                      <dt><span>請求額（合計）</span></dt>
                      <dd>¥110,000</dd>
                    </dl>
                    <div class="apply-step3-detail-content">
                      <p>本コースはReスキル給付金の対象コースです。受講時と受講完了時にハローワークで手続きを行う必要があります。<br>給付金は最大￥70,00です。給付金は受講完了時に支払いが行われます。<br><a href="#">給付金の詳細に関してはこちら →</a></p>
                      <p>支払いを完了することにより、これらのサービス規約に同意したものとみなされます。</p>
                    </div>
                  </div>
                </div>
                <div class="apply-step3-bottom">
                  <div>
                    <h4 class="apply-step3-head">名前</h4>
                    <div class="pay-apply-type">
                        <div><RadioSelect>個人</RadioSelect></div>
                        <div><RadioSelect>法人</RadioSelect></div>
                    </div>
                  </div>
                  <div>
                    <h4 class="apply-step3-head">お申し込みコース</h4>
                    <div class="pay-apply-type">
                        <div><RadioSelect>個人</RadioSelect></div>
                        <div><RadioSelect>法人</RadioSelect></div>
                    </div>
                  </div>
                  <div class="form-consent">
                    <div><CheckBox>プライバシーポリシーに同意する</CheckBox></div>
                    <div><CheckBox>キャンセルーポリシーに同意する</CheckBox></div>
                  </div>
                </div>
              </div>
            </div>
            <div>
              <h3 class="apply-form-head">お申し込み後の流れ</h3>
              <ul class="pay-flow">
                <li>
                  <div class="pay-flow-circle">
                    <div>
                      <p class="pay-flow-num">STEP 01</p>
                      <h4 class="pay-flow-head">メールを受け取る</h4>
                    </div>
                  </div>
                  <p>振込情報などが<br>記載されています。</p>
                </li>
                <li>
                  <div class="pay-flow-circle">
                    <div>
                      <p class="pay-flow-num">STEP 02</p>
                      <h4 class="pay-flow-head">振込を完了する</h4>
                    </div>
                  </div>
                  <p>お振込が完了すると、<br>コンテンツが閲覧可能になります。</p>
                </li>
                <li>
                  <div class="pay-flow-circle">
                    <div>
                      <p class="pay-flow-num">STEP 03</p>
                      <h4 class="pay-flow-head">学習を始める</h4>
                    </div>
                  </div>
                  <p>お振込後1営業日以内に<br>コンテンツが確認可能になります。</p>
                </li>
              </ul>
            </div>
          </div>
            <div class="apply-form-btn">
              <SendForm>申し込み内容を送信する</SendForm>
            </div>
        </div>
      </div>
    </section>
</template>

<script>
    import RadioSelect from '~/components/atoms/forms/RadioSelect.vue'
    import CheckBox from '~/components/atoms/forms/CheckBox.vue'
    import InputText from '~/components/atoms/forms/InputText.vue'

    export default {
        components: {
            RadioSelect,
            CheckBox,
            InputText
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- section --> apply */

.sec--pay-apply {
  padding: vw-sp(100) 0 vw-sp(120) 0;
  background-image: url(~assets/img/pay/apply-bg.jpg);
  background-size: cover;
}

@media screen and (min-width: $breakpoint1) {

  .sec--pay-apply {
    padding: vw-pc(115) 0 vw-pc(130) 0;
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--pay-apply {
    padding: 115px 0 130px 0;
  }
}
/* ---------------------------------- component --> apply-form-box */

.apply-form-box {
  margin-bottom: vw-sp(80);
  padding: vw-sp(65) vw-sp(40) vw-sp(80) vw-sp(40);
  width: 100%;
  background-color: $color-base;
  box-shadow: 0px 5px 30px 0px rgba(0, 0, 0, 0.2);
}

.apply-form-box:last-child {
  margin-bottom: 0;
}

.apply-form-head {
  margin-bottom: 2em;
  font-size: vw-sp(34);
  font-weight: 700;
  text-align: center;
  line-height: 1.6em;
  letter-spacing: .2em;
}

.apply-form-box__in {
  margin: 0 auto;
  width: 100%;
}

@media screen and (min-width: $breakpoint1) {

  .apply-form-box {
    margin-bottom: vw-pc(50);
    padding: vw-pc(55) vw-pc(100) vw-pc(70) vw-pc(100);
  }

  .apply-form-head {
    font-size: vw-pc(24);
  }

  .apply-form-box__in {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    width: vw-pc(1000);
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-form-box {
    margin-bottom: 50px;
    padding: 55px 100px 70px 100px;
  }

  .apply-form-head {
    font-size: 24px; font-size: 2.4rem;
  }

  .apply-form-box__in {
    width: 1000px;
  }
}
/* ---------------------------------- component --> form-step */

.form-step {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: 0 auto vw-sp(55) auto;
  width: vw-sp(580);
}

.form-step li {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  width: vw-sp(130);
  height: vw-sp(130);
  background-color: #e9f9f2;
  border-radius: 50%;
  p {
    margin-top: .2em;
    color: $color-base;
    font-family: $font2;
    font-size: vw-sp(28);
    font-weight: 700;
    text-align: center;
    line-height: 1.4em;
  }
}

.form-step li.is-active {
  background-color: $color-main;
}

.form-step li:after {
  content: '・・・・・・';
  position: absolute;
  top: 50%;
  left: 103%;
  color: $color-main;
  font-family: $font1;
  font-weight: 700;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
}

.form-step li:last-child:after {
  content: none;
}

@media screen and (min-width: $breakpoint1) {

  .form-step {
    margin: 0 auto vw-pc(45) auto;
    width: vw-pc(510)
  }

  .form-step li {
    width: vw-pc(100);
    height: vw-pc(100);
    p {
      font-size: vw-pc(18);
    }
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-step {
    margin: 0 auto 45px auto;
    width: 510px
  }

  .form-step li {
    width: 100px;
    height: 100px;
    p {
      font-size: 18px; font-size: 1.8rem;
    }
  }
}
/* ---------------------------------- component --> step2 --> pay-input */

.pay-input {
  margin-bottom: vw-sp(50);
}

.pay-input dt {
  display: block;
  width: 100%;
  margin-bottom: .7em;
  font-weight: 700;
}

.pay-input dd {
  display: block;
  width: 100%;
}

.pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
  padding: 1em 1em;
  background-color: #f8f8f8;
  border: 1px solid $color-main;
  border-radius: .5em;
  width: 100%;
  max-width: 100%;
  color: $color-text;
  font-family: $font1;
  font-size: vw-sp(25);
  font-weight: 700;
  letter-spacing: .1em;
}

@media screen and (min-width: $breakpoint1) {

  .pay-input {
    margin-bottom: vw-pc(40);
    width: vw-pc(485);
  }

  .pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
    font-size: vw-pc(15);
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-input {
    margin-bottom: 40px;
    width: 485px;
  }

  .pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
    font-size: 15px;
  }
}


/* ---------------------------------- component --> step2 --> pay-input */


.apply-step2-desc {
  padding-top: 1.5em;
  padding-left: 1em;
  text-indent: -1em;
  font-size: .81em;
  line-height: 1.6em;
}

.apply-step2-desc:before {
  content: '※';
}

@media screen and (min-width: $breakpoint1) {

  .apply-step2-desc {
    text-align: center;
  }
}




/* ---------------------------------- component --> form-consent */

.form-consent {
  margin: vw-sp(50) 0 vw-sp(60) 0;
  font-size: vw-sp(26);
  font-weight: 700;
  text-align: center;
}

.apply-step3-bottom .form-consent {
  text-align: left;
}

.apply-step3-bottom .form-consent > div {
  margin-bottom: 1.2em;
}

.apply-form input[type="checkbox"] {
  display: none;
}

.apply-form input[type="checkbox"] + span {
  position: relative;
  display: inline-block;
  padding: 0 0 0 2em;
  cursor: pointer;
}

.apply-form input[type="checkbox"] + span::before {
  position: absolute;
  content: '';
  top: 50%;
  left: 0;
  display: block;
  width: 1.3em;
  height: 1.3em;
  background-color: #f8f8f8;
  border: 1px solid $color-main;
  border-radius: 0;
  transform: translateY(-50%);
}

.apply-form input[type="checkbox"]:checked + span::after {
  position: absolute;
  content: '';
  top: 50%;
  left: 0;
  display: block;
  width: 1.3em;
  height: .6em;
  margin-top: -.2em;
  border-left: vw-sp(5) solid $color-main;
  border-bottom: vw-sp(5) solid $color-main;
  transform: translateY(-50%) rotate(-45deg);
}


@media screen and (min-width: $breakpoint1) {

  .form-consent {
    margin: vw-pc(30) 0 vw-pc(40) 0;
    font-size: vw-pc(16);
  }

  .apply-form input[type="checkbox"]:checked + span::after {
    border-left: vw-pc(3) solid $color-main;
    border-bottom: vw-pc(3) solid $color-main;
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-consent {
    margin: 30px 0 40px 0;
    font-size: 16px; font-size: 1.6rem;
  }

  .apply-form input[type="checkbox"]:checked + span::after {
    border-left: 3px solid $color-main;
    border-bottom: 3px solid $color-main;
  }
}

/* ---------------------------------- component --> step3 */


.apply-step3 {
  margin-bottom: vw-sp(120);
}

.apply-step3-top {
  margin-bottom: vw-sp(60);
  width: 100%;
}

.apply-step3-bottom {
  width: 100%;
}


@media screen and (min-width: $breakpoint1) {

  .apply-step3 {
    display: flex;
    justify-content: space-between;
    margin-bottom: vw-pc(60);
  }

  .apply-step3-top {
    margin-bottom: 0;
    width: vw-pc(485);
  }

  .apply-step3-bottom {
    width: vw-pc(570);
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-step3 {
    margin-bottom: 60px;
  }

  .apply-step3-top {
    width: 485px;
  }

  .apply-step3-bottom {
    width: 470px;
  }
}

.apply-step3-head {
  margin-bottom: .7em;
  font-weight: 700;
}

.apply-step3-detail {
  padding: vw-sp(35) vw-sp(30);
  background-color: #f8f8f8;
  border-radius: vw-sp(15);
}

.apply-step3-detail-head {
  margin-bottom: .5em;
  font-size: vw-sp(30);
  font-weight: 700;
  line-height: 1.5em;
}

.apply-step3-prices {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-bottom: 1.2em;
  dt {
    display: flex;
    align-items: center;
    width: vw-sp(220);
    font-size: .81em;
    font-weight: 700;
    line-height: 1.6em;
    span:after {
      content: '：';
    }
  }
  dd {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    width: calc(100% - #{vw-sp(220)});
    font-family: $font2;
    font-size: 1.25em;
    font-weight: 700;
    line-height: 1.6em;
  }
}

.apply-step3-detail-content {
  padding-top: 1.5em;
  border-top: vw-sp(3) solid $color-text;
}

.apply-step3-detail-content p {
  margin-bottom: 1.5em;
  font-size: .81em;
  line-height: 1.8em;
  a {
    display: inline-block;
    padding-bottom: .3em;
    border-bottom: 1px solid $color-text;
  }
  a:hover {
    opacity: .7;
  }
}

.apply-step3-detail-content p:last-child {
  margin-bottom: 0;
}

.apply-step3-bottom > div {
  margin-bottom: vw-sp(50);
}

.apply-step3-bottom > div:last-child {
  margin-bottom: 0;
}

.pay-apply-type {
  display: flex;
  justify-content: space-between;
  > div {
    width: vw-sp(300);
  }
}

@media screen and (min-width: $breakpoint1) {

  .apply-step3-detail {
    padding: vw-pc(25) vw-pc(30);
    border-radius: vw-pc(10);
  }

  .apply-step3-detail-head {
    font-size: vw-pc(20);
  }

  .apply-step3-prices {
    dt {
      width: 50%;
    }
    dd {
      width: 50%;
    }
  }

  .apply-step3-detail-content {
    border-top: vw-pc(2) solid $color-text;
  }

  .apply-step3-bottom > div {
    margin-bottom: vw-pc(40);
  }

  .pay-apply-type {
    > div {
      width: vw-pc(275);
    }
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-step3-detail {
    padding: 25px 30px;
    border-radius: 10px;
  }

  .apply-step3-detail-head {
    font-size: 20px; font-size: 2.0rem;
  }

  .apply-step3-detail-content {
    border-top: 2px solid $color-text;
  }

  .apply-step3-bottom > div {
    margin-bottom: 40px;
  }

  .pay-apply-type {
    > div {
      width: 225px;
    }
  }
}


.pay-apply-type label {
  margin-bottom: vw-sp(20);
}

.pay-apply-type label:last-child {
  margin-bottom: 0;
}

.pay-apply-type span {
  position: relative;
  display: flex;
  align-items: center;
  padding: 0 vw-sp(50) 0 vw-sp(110);
  width: 100%;
  background-color: #e9f9f2;
  border-radius: .5em;
  height: vw-sp(90);
  font-size: vw-sp(28);
  font-weight: 700;
  cursor: pointer;
}

.pay-apply-type input[type="radio"]:checked + span {
  background-color: $color-main;
  color: $color-base;
}

.pay-apply-type input[type="radio"] {
  display: none;
}

.pay-apply-type input[type="radio"] + span::before {
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(30);
  display: block;
  width: vw-sp(50);
  height: vw-sp(50);
  background-color: $color-base;
  border-radius: 50%;
  transform: translateY(-50%);
}

.pay-apply-type input[type="radio"]:checked + span::after {
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(30);
  transform: translateY(-50%);
  background-color: $color-text;
  border-radius: 50%;
  width: vw-sp(30);
  height: vw-sp(30);
  border: vw-sp(10) solid $color-base;
  display: block;
}

@media screen and (min-width: $breakpoint1) {

  .pay-apply-type label {
    margin-bottom: vw-pc(10);
  }

  .pay-apply-type span {
    padding: 0 vw-pc(50) 0 vw-pc(75);
    height: vw-pc(60);
    border-radius: .5em;
    font-size: vw-pc(18);
  }

  .pay-apply-type input[type="radio"] + span::before {
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
  }

  .pay-apply-type input[type="radio"]:checked + span::after {
    left: vw-pc(20);
    width: vw-pc(16);
    height: vw-pc(16);
    border: vw-pc(8) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-apply-type label {
    margin-bottom: 10px;
  }

  .pay-apply-type span {
    padding: 0 50px 0 75px;
    height: 60px;
    font-size: 18px; font-size: 1.8rem;
  }

  .pay-apply-type input[type="radio"] + span::before {
    left: 20px;
    width: 32px;
    height: 32px;
  }

  .pay-apply-type input[type="radio"]:checked + span::after {
    left: 20px;
    width: 16px;
    height: 16px;
    border: 8px solid $color-base;
  }
}

/* ---------------------------------- component --> pay-flow */

.pay-flow {
  width: 100%;
}

.pay-flow li {
  position: relative;
  margin-bottom: vw-sp(60);
  width: 100%;
  z-index: 2;
  > p {
    position: absolute;
    font-size: vw-sp(20);
    line-height: 1.8em;
  }
}

.pay-flow-circle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: vw-sp(240);
  height: vw-sp(240);
  background-color: #f8f8f8;
  border-radius: 50%;
  text-align: center;
  z-index: 2;
}

.pay-flow-num {
  display: inline-block;
  margin-bottom: .8em;
  font-family: $font2;
  font-size: vw-sp(28);
  font-weight: 700;
  text-align: center;
  @include marker;
}

.pay-flow-head {
  font-size: vw-sp(22);
  font-weight: 700;
  text-align: center;
}

@media screen and (max-width: $breakpoint1-max) {

  .pay-flow li:after {
    content: '';
    position: absolute;
    top: vw-sp(115);
    left: vw-sp(120);
    width: vw-sp(20);
    height: 80%;
    background-color: #f8f8f8;
    transform: translateX(-50%);
    z-index: -1;
  }

  .pay-flow li:last-child::after {
    content: none;
  }

  .pay-flow li {
    > p {
      top: 50%;
      left: vw-sp(260);
      transform: translateY(-50%);
      white-space: nowrap;
    }
  }

}

@media screen and (min-width: $breakpoint1) {

  .pay-flow {
    position: relative;
    display: flex;
    justify-content: space-between;
    align-items: center;
    margin: 0 auto;
    width: vw-pc(835);
  }

  .pay-flow li {
    margin-bottom: 0;
    padding-bottom: vw-pc(55);
    width: vw-pc(190);
    > p {
      position: absolute;
      bottom: 0;
      left: 50%;
      margin-top: 1em;
      font-size: vw-pc(13);
      text-align: center;
      transform: translateX(-50%);
      white-space: nowrap;
    }
  }

  .pay-flow:after {
    content: '';
    position: absolute;
    top: vw-pc(85);
    left: 50%;
    width: 90%;
    height: vw-pc(10);
    background-color: #f8f8f8;
    transform: translateX(-50%);
  }

  .pay-flow-circle {
    width: vw-pc(190);
    height: vw-pc(190);
  }

  .pay-flow-num {
    font-size: vw-pc(18);
  }

  .pay-flow-head {
    font-size: vw-pc(16);
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-flow {
    width: 735px;
  }

  .pay-flow li {
    padding-bottom: 55px;
    width: 180px;
    > p {
      font-size: 13px; font-size: 1.3rem;
    }
  }

  .pay-flow:after {
    top: 85px;
    height: 10px;
  }

  .pay-flow-circle {
    width: 180px;
    height: 180px;
  }

  .pay-flow-num {
    font-size: 18px; font-size: 1.8rem;
  }

  .pay-flow-head {
    font-size: 16px; font-size: 1.6rem;
  }
}

/* ---------------------------------- component --> apply-form-btn */

.apply-form-btn {
  margin: 0 auto;
  width: vw-sp(500);
  .cmn-btn {
    border: none !important;
  }
}

.form-submit-btn {
  display: block;
  width: 100%;
  height: 100%;
  color: $color-base;
  font-size: vw-sp(26);
  font-weight: 700;
  letter-spacing: .1em;
}

.form-submit-btn:hover {
  color: #ff9f01;
}

@media screen and (min-width: $breakpoint1) {

  .apply-form-btn {
    margin-top: vw-pc(50);
    width: vw-pc(480);
  }

  .form-submit-btn {
    font-size: vw-pc(16);
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-form-btn {
    margin-top: 50px;
    width: 480px;
  }

  .form-submit-btn {
    font-size: 16px; font-size: 1.6rem;
  }
}


</style>
