<template>
    <section class="sec sec--pay-hero">
      <div>
        <div class="sec__in">
          <h2 class="pay-hero-head">ディープラーニング<br class="br--sp">ハンズオンコースの<br>申し込みフォーム</h2>
          <p class="pay-hero-desc">コースの購入は支払い後に完了し、<br class="br--sp">購入コンテンツを確認することができます</p>
          <div class="form-label">
            <p>簡単<span>3ステップ</span>でお申し込み</p>
          </div>
          <ul class="form-step">
            <li class="is-active"><p>STEP<br>01</p></li>
            <li><p>STEP<br>02</p></li>
            <li><p>STEP<br>03</p></li>
          </ul>
        </div>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- section --> hero */

.sec--pay-hero {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  max-width: 100%;
  height: vw-sp(800);
}

.sec--pay-hero:before,
.sec--pay-hero:after {
  content: '';
  position: absolute;
  top: 50%;
  display: inline-block;
  background-size: contain;
  background-repeat: no-repeat;
  transform: translateY(-50%);
  z-index: -1;
}

.sec--pay-hero:before {
  left: vw-sp(-80);
  width: vw-sp(308);
  height: vw-sp(750);
  background-image: url(~assets/img/bg/bg-left.png);
}

.sec--pay-hero:after {
  right: vw-sp(-80);
  width: vw-sp(330);
  height: vw-sp(726);
  background-image: url(~assets/img/bg/bg-right.png);
}

@media screen and (min-width: $breakpoint1) {

  .sec--pay-hero {
    align-items: flex-start;
    top: vw-pc(120);
    height: vw-pc(590);
  }

  .sec--pay-hero:before {
    left: 0;
    width: vw-pc(308);
    height: vw-pc(750);
  }

  .sec--pay-hero:after {
    right: 0;
    width: vw-pc(330);
    height: vw-pc(726);
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--pay-hero {
    top: 120px;
    height: 590px;
  }

  .sec--pay-hero:before {
    width: 308px;
    height: 750px;
  }

  .sec--pay-hero:after {
    width: 330px;
    height: 726px;
  }
}
/* ---------------------------------- component --> form-label */

.form-label {
  margin: vw-sp(40) 0;
  text-align: center;
  p {
    display: inline-block;
    padding: .8em 2em;
    background-color: $color-main;
    border-radius: vw-sp(45);
    color: $color-base;
    font-size: vw-sp(28);
    text-align: center;
    font-weight: 700;
    letter-spacing: .2em;
    span {
      color: #f9ff49;
    }
  }
}

@media screen and (min-width: $breakpoint1) {

  .form-label {
    margin: vw-pc(30) 0;
    p {
      padding: .9em 3em;
      border-radius: vw-pc(25);
      font-size: vw-pc(18);
    }
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-label {
    margin: 30px 0;
    p {
      border-radius: 25px;
      font-size: 18px; font-size: 1.8rem;
    }
  }
}


/* ---------------------------------- component --> hero */

.pay-hero-head {
  margin-bottom: 1.2em;
  font-size: vw-sp(46);
  font-weight: 700;
  text-align: center;
  line-height: 1.8em;
  letter-spacing: .2em;
}

@media screen and (min-width: $breakpoint1) {

  .pay-hero-head {
    font-size: vw-pc(36);
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-hero-head {
    font-size: 36px; font-size: 3.6rem;
  }
}

.pay-hero-desc {
  font-size: 1.125em;
  font-weight: 700;
  text-align: center;
  line-height: 1.8em;
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
/* ---------------------------------- heading */

.cmn-head--style {
  margin-bottom: vw-sp(100);
}

@media screen and (min-width: $breakpoint1) {

  .cmn-head--style {
    margin-bottom: vw-pc(70);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-head--style {
    margin-bottom: 70px;
  }
}


</style>
