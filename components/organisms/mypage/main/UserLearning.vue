<template>
    <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">学習中のコンテンツ</h2>
        </div>
        <div class="learn-box">
          <div class="learn-box-top">
              <div class="learn-box-image">
                <img src="~/assets/img/detail/view.jpg" class="img--fit" alt="course">
              </div>
              <div class="learn-box-content">
                <h3 class="mymain-subhead">長期コース - 機械学習の数学</h3>
                <p>機械学習の基礎、Webアプリケーションについて学び、0からプロトタイプを作り上げる技術力を身につける。</p>
              </div>
          </div>
          <div class="learn-box-bottom">
            <div>
              <p class="learn-box-progress"><span>2</span>/50 レッスン完了 !</p>
              <div class="learn-box-btn">
                <div class="mycmn-btn mycmn-btn--line mycmn-btn--hign">
                  <div></div>
                  <a href="#"><span>学習を再開する</span></a>
                </div>
              </div>
            </div>
          </div>
        </div>
      </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ---------------------------------- learn-box */

.learn-box {
  border: vw-sp(4) solid $color-main;
  background-color: #e9f9f2;
}

.learn-box-top {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: 0;
  padding: vw-sp(30) vw-sp(15) vw-sp(20) vw-sp(30);
  width: 100%;
  background-color: $color-base;
}

.learn-box-top:after {
  content: '';
  position: absolute;
  width: 0;
  height: 0;
  border-style: solid;
}

.learn-box-image {
  width: vw-sp(140);
}

.learn-box-content {
  width: vw-sp(470);
  p {
    line-height: 1.6em;
  }
}

.learn-box-name {
  font-size: 1.25em;
  font-weight: 700;
  text-align: center;
  line-height: 1.5em;
}

.learn-box-bottom {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: vw-sp(60) vw-sp(40) vw-sp(40) vw-sp(40);
  width: 100%;
  height: 100%;
}

.learn-box-progress {
  margin-bottom: vw-sp(30);
  color: $color-orange;
  font-family: $font2,$font1;
  text-align: center;
  font-weight: 700;
  span {
    font-size: 1.5em;
  }
}

.learn-box-btn {
  margin: 0 auto;
  width: vw-sp(460);
}

@media screen and (max-width: $breakpoint1-max) {

  .learn-box-top:after {
    top: 100%;
    left: 0;
    border-width: 0 vw-sp(678) vw-sp(40) 0;
    border-color: transparent $color-base transparent transparent;
  }

}

@media screen and (min-width: $breakpoint1) {

  .learn-box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: vw-pc(159);
    border: vw-pc(2) solid $color-main;
  }

  .learn-box-top {
    align-items: center;
    padding: vw-pc(30) vw-pc(15) vw-pc(30) vw-pc(30);
    width: vw-pc(810);
  }

  .learn-box-top:after {
    top: 0;
    left: 100%;
    border-width: vw-pc(155) vw-pc(40) 0 0;
    border-color: $color-base transparent transparent transparent;
  }

  .learn-box-image {
    width: vw-pc(142);
  }

  .learn-box-content {
    width: vw-pc(590);
  }

  .learn-box-bottom {
    padding: 0 vw-pc(30);
    width: vw-pc(360);
    height: 100%;
  }

  .learn-box-progress {
    margin-bottom: vw-pc(15);
  }

  .learn-box-btn {
    width: vw-pc(300);
  }
}

</style>