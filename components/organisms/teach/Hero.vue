<template>
    <div class="teach-hero">
      <div class="teach-hero__in">
        <div class="teach-hero-content">
          <p class="teach-hero-catch">新しい技術を学び<br class="br--sp"><strong><span>世</span><span>界</span><span>に</span><span>届</span><span>け</span><span>る</span><span>人</span><span>材</span></strong></p>
          <div class="teach-hero-header"><h2 class="teach-hero-head">認定クリエイター</h2></div>
          <div class="teach-hero-btn">
            <div class="cmn-btn cmn-btn--main cmn-btn--low">
              <div></div>
              <p>認定クリエイターに応募する（無料）</p>
            </div>
          </div>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- hero */

.teach-hero {
  position: relative;
  height: vw-sp(1000);
  background-image: url(~assets/img/teach/teach-hero_sp.jpg);
  background-size: cover;
  background-position: center bottom;
}

.teach-hero__in {
  position: relative;
  margin: 0 auto;
  width: vw-sp(700);
}

.teach-hero-content {
  padding-top: vw-sp(60);
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .teach-hero {
    height: vw-pc(600);
    background-image: url(~assets/img/teach/teach-hero.jpg);
    background-position: center;
  }

  .teach-hero__in {
    width: vw-pc(1400);
  }

  .teach-hero-content {
    padding-top: vw-pc(160);
    text-align: left;
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-hero {
    height: 600px;
  }

  .teach-hero__in {
    width: 1400px;
  }

  .teach-hero-content {
    padding-top: 160px;
  }
}

/* ----------------- テキスト - */


.teach-hero-catch {
  position: relative;
  margin-bottom: 1em;
  color: $color-base;
  font-size: vw-sp(48);
  font-weight: 700;
  text-align: center;
  line-height: 2em;
  letter-spacing: .2em;
  white-space: nowrap;
}

.teach-hero-catch strong {
  color: #f9ff49;
  span {
    position: relative;
  }

  span:before {
    position: absolute;
    top: -1.1em;
    left: 50%;
    content: '・';
    color: #f9ff49;
    font-weight: 700;
    transform: translateX(-50%);
  }
}


@media screen and (min-width: $breakpoint1) {


  .teach-hero-catch {
    font-size: vw-pc(36);
    text-align: left;
    line-height: 1.8em;
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-hero-catch {
    font-size: 36px; font-size: 3.6rem;
  }
}


.teach-hero-header {
  position: relative;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  padding: 0 2em;
  background-color: #29b2e6;
  height: vw-sp(120);
  transform: skewX(-35deg);
  z-index: 2;
}

.teach-hero-header:after {
  content: '';
  position: absolute;
  top: vw-sp(-35);
  left: vw-sp(-15);
  display: inline-block;
  width: vw-sp(68);
  height: vw-sp(145);
  background-image: url(~assets/img/teach/hero-illust.png);
  background-size: contain;
  background-repeat: no-repeat;
  transform: skewX(35deg);
  z-index: 2;
}

.teach-hero-head {
  padding-left: .5em;
  color: $color-base;
  font-size: vw-sp(46);
  font-weight: 700;
  letter-spacing: .2em;
  transform: skewX(35deg);
}

@media screen and (min-width: $breakpoint1) {

  .teach-hero-header {
    left: vw-pc(30);
    height: vw-pc(90);
    padding: 0 4em;
  }

  .teach-hero-header:after {
    top: vw-pc(-25);
    left: vw-pc(-15);
    width: vw-pc(48);
    height: vw-pc(102);
  }

  .teach-hero-head {
    font-size: vw-pc(36);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-hero-header {
    left: 30px;
    height: 90px;
  }

  .teach-hero-header:after {
    top: -25px;
    left: -15px;
    width: 48px;
    height: 102px;
  }

  .teach-hero-head {
    font-size: 36px; font-size: 3.6rem;
  }
}


/* ---------------------------------- btn */

.teach-hero-btn {
  margin: vw-sp(40) auto 0 auto;
  width: vw-sp(620);
}

@media screen and (min-width: $breakpoint1) {

  .teach-hero-btn {
    margin: vw-pc(30) 0 0 0;
    width: vw-pc(560);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-hero-btn {
    margin: 30px 0 0 0;
    width: 560px;
  }
}
/* ---------------------------------- cmn btn */

.cmn-btn {
  position: relative;
  font-family: $font2,$font1;
  display: inline-flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  border: vw-sp(5) solid $color-base !important;
  box-shadow: 0px 10px 10px 0px rgba(0, 0, 0, 0.1);
  text-align: center;
  overflow: hidden;
  cursor: pointer;
  p {
    line-height: 1.4em;
  }
}

.cmn-btn--short,
.cmn-btn--low {
  border-radius: 2.5em;
}

.cmn-btn--high {
  border-radius: 3.5em;
}

.cmn-btn--short,
.cmn-btn--short p,
.cmn-btn--short > div {
  height: vw-sp(80);
}

.cmn-btn--low,
.cmn-btn--low p,
.cmn-btn--low > div {
  height: vw-sp(90);
}

.cmn-btn--high,
.cmn-btn--high a,
.cmn-btn--high > div {
  height: vw-sp(120);
}

.cmn-btn--alte,
.cmn-btn--alte a,
.cmn-btn--alte > div {
  height: vw-sp(130);
  border-radius: 3.5em;
}

.cmn-btn a,
.cmn-btn p {
  position:relative;
  display: flex;
  justify-content: center;
  align-items: center;
  color: $color-base;
  width: 100%;
  font-size: vw-sp(28);
  font-weight: 700;
  text-decoration:none;
  transition:all .5s ease;
  z-index: 2;
  small {
    font-size: 0.86em;
  }
}

.cmn-btn > div {
  position: absolute;
  width: 100%;
  top: 0;
  left: -100%;
  background-color: $color-base;
  transition:all .5s ease;
  z-index: 1;
}

@media screen and (max-width: $breakpoint1-max) {

  .cmn-btn--alte,
  .cmn-btn--alte a,
  .cmn-btn--alte > div {
    p {
      flex-wrap: wrap;
    }
    span {
      display: block;
      width: 100%;
    }
    span:nth-child(1) {
      margin-bottom: .2em;
    }
  }
}

@media screen and (min-width: $breakpoint1) {

  .cmn-btn--short,
  .cmn-btn--short p,
  .cmn-btn--short > div {
    height: vw-pc(60);
  }


  .cmn-btn--low,
  .cmn-btn--low p,
  .cmn-btn--low > div {
    height: vw-pc(70);
  }

  .cmn-btn--high,
  .cmn-btn--high a,
  .cmn-btn--high > div {
    height: vw-pc(100);
  }

  .cmn-btn--alte,
  .cmn-btn--alte p,
  .cmn-btn--alte > div {
    height: vw-pc(70);
    border-radius: 2.5em;
  }


  .cmn-btn {
    border: vw-pc(3) solid $color-base !important;
  }

  .cmn-btn a,
  .cmn-btn p {
    font-size: vw-pc(24);
    small {
      font-size: 0.66em;
    }
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-btn--short,
  .cmn-btn--short p,
  .cmn-btn--short > div {
    height: 60px;
  }

  .cmn-btn--low,
  .cmn-btn--low p,
  .cmn-btn--low > div {
    height: 70px;
  }

  .cmn-btn--high,
  .cmn-btn--high a,
  .cmn-btn--high > div {
    height: 100px;
  }

  .cmn-btn--alte,
  .cmn-btn--alte p,
  .cmn-btn--alte > div {
    height: 70px;
  }

  .cmn-btn {
    border: 3px solid $color-base !important;
  }

  .cmn-btn a,
  .cmn-btn p {
    font-size: 24px; font-size: 2.4rem;
  }
}

.cmn-btn a:before {
  content: '';
  display: inline-block;
  margin-right: .5em;
  background-size: contain;
  background-repeat: no-repeat;
}

.cmn-btn--main {
  background-image: -moz-linear-gradient( 0deg, rgb(255,158,0) 0%, rgb(255,181,23) 100%);
  background-image: -webkit-linear-gradient( 0deg, rgb(255,158,0) 0%, rgb(255,181,23) 100%);
}

@media all and (-ms-high-contrast: none){
  .cmn-btn--main {
    background-image: none;
    background-color: rgb(255,158,0);
  }
}

.cmn-btn--main:hover p {
  color: #ff9e00;
}

.cmn-btn:hover > div {
  left: 0;
  background-color: $color-base;
}




.cmn-btn--back span {
  position: relative;
  padding-left: 1.2em;
}

.cmn-btn--back span:before {
  position: absolute;
  top: 50%;
  left: 0;
  content: '';
display: inline-block;
width: vw-sp(18);
height: vw-sp(9);
background-image: url(~assets/img/common/back_w.png);
background-size: contain;
background-repeat: no-repeat;
-webkit-transform: translateY(-50%);
transform: translateY(-50%);
}

.cmn-btn--back:hover span:before {
  background-image: url(~assets/img/common/back_o.png);
}


@media screen and (min-width: $breakpoint1) {

  .cmn-btn--back span:before {
  width: vw-pc(18);
  height: vw-pc(9);
  }
}


@media screen and (min-width: $breakpoint2) {

  .cmn-btn--back span:before {
  width: 18px;
  height: 9px;
  }
}

</style>
