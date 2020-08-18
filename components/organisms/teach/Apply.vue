<template>
    <section id="apply" class="sec sec--teach-apply">
      <div class="sec__in">
          <h2 class="teach-apply-head">まずは認定クリエイターに<br class="br--sp">応募してみましょう！</h2>
          <div class="teach-apply-content">
            <p>教育で世の中を変えたい思いさえあれば、<br>誰でも認定クリエイターに<br class="br--sp">なることができます。<br>一緒によりよい教育のコンテンツを<br class="br--sp">作成していきませんか？</p>
          </div>
          <div class="teach-apply-btn">
            <div class="cmn-btn cmn-btn--main cmn-btn--low">
              <div></div>
              <p>認定クリエイターに応募する（無料）</p>
            </div>
          </div>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- apply --> section */

.sec--teach-apply {
  padding: vw-sp(100) 0;
  background-image: url(~assets/img/teach/apply-bg.jpg);
  background-size: cover;
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-apply {
    padding: vw-pc(115) 0;;
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-apply {
    padding: 115px 0;
  }
}


/* ---------------------------------- apply --> heading */

.teach-apply-head {
  margin-bottom: .5em;
  background: linear-gradient( to right,  #1dd5e6 25%, #46aef7 75% );
  color: transparent;
  -webkit-background-clip: text;
  font-size: vw-sp(40);
  font-weight: 700;
  text-align: center;
  line-height: 1.6em;
  letter-spacing: .2em;
}

@media all and (-ms-high-contrast: none) { /* IE10,11用 */
  .teach-apply-head {
    background: none;
    color: #1dd5e6;
  }
}

@media screen and (min-width: $breakpoint1) {

  .teach-apply-head {
    font-size: vw-pc(30);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-apply-head {
    font-size: 30px; font-size: 3.0rem;
  }
}

/* ---------------------------------- apply --> conponent */

.teach-apply-content p {
  font-size: 1.125em;
  font-weight: 700;
  text-align: center;
  line-height: 2em;
}

.teach-apply-btn {
  margin: vw-sp(40) auto 0 auto;
  width: vw-sp(640);
}

@media screen and (min-width: $breakpoint1) {

  .teach-apply-btn {
    margin: vw-pc(30) auto 0 auto;
    width: vw-pc(560);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-apply-btn {
    margin: 30px auto 0 auto;
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

/* ---------------------------------- btn */

.cta-btn {
  margin: vw-sp(60) auto 0 auto;
  width: vw-sp(660);
}

@media screen and (min-width: $breakpoint1) {

  .cta-btn {
    margin: vw-pc(65) auto 0 auto;
    width: vw-pc(600);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cta-btn {
    margin: 65px auto 0 auto;
    width: 600px;
  }
}

</style>
