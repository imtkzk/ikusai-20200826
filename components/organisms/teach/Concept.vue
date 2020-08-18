<template>
    <section id="concept" class="sec sec--teach-concept">
      <div class="sec__in">
        <div class="cmn-head cmn-head--teach-concept">
          <p class="cmn-head__en">CONCEPT</p>
          <h2 class="cmn-head__jp">認定クリエイターとは？</h2>
        </div>
        <ul class="what">
          <li>
            <div><div class="what-image">
              <img src="~/assets/img/teach/concept01.jpg" srcset="~/assets/img/teach/concept01.jpg 1x,~/assets/img/teach/concept01-2x.jpg 2x" class="img--fit" alt="あなたの興味、知識で世界の学びを加速させる">
            </div>
            <div class="what-content">
              <h3 class="what-head">あなたの興味、知識で<br class="br--sp">世界の学びを加速させる</h3>
              <ul class="what-list">
                <li>手書き数学で難しい数学もわかりやすく解説</li>
                <li>プログラミングは実際に自身で動かしながら学び、実力がつく設計</li>
                <li>動画と資料の両方で学ぶため、わからなかった部分は何度も見返すことが可能</li>
              </ul>
            </div></div>
          </li>
          <li>
            <div><div class="what-image">
              <img src="~/assets/img/teach/concept02.jpg" srcset="~/assets/img/teach/concept02.jpg 1x,~/assets/img/teach/concept02-2x.jpg 2x" class="img--fit" alt="0からでも始められるikus.aiプロデュース">
            </div>
            <div class="what-content">
              <h3 class="what-head">0からでも始められる<br class="br--sp">ikus.aiプロデュース</h3>
              <ul class="what-list">
                <li>他の受講生と学習を進めることができるチーム学習が選べる</li>
                <li>モチベーションを高く維持し、学習を進めることができる</li>
                <li>わからない点があった時に、お互い助け合うことができる</li>
              </ul>
            </div></div>
          </li>
          <li>
            <div><div class="what-image">
              <img src="~/assets/img/teach/concept03.jpg" srcset="~/assets/img/teach/concept03.jpg 1x,~/assets/img/teach/concept03-2x.jpg 2x" class="img--fit" alt="新たな教育のエコシステムを形成する">
            </div>
            <div class="what-content">
              <h3 class="what-head">新たな教育の<br class="br--sp">エコシステムを形成する</h3>
              <ul class="what-list">
                <li>実際に使える技術が身についていることを実感できる</li>
                <li>レベルを可視化し、自分の実力をいつでも確認することができる</li>
                <li>レベルに応じた適切な学ぶ内容を決めることができる</li>
              </ul>
            </div></div>
          </li>
        </ul>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- concept --> section */

.sec--teach-concept {
  padding: vw-sp(120) 0;
  background-image: url(~assets/img/teach/concept-bg.jpg);
  background-size: cover;
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-concept {
    padding: vw-pc(110) 0 vw-pc(120) 0;;
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-concept {
    padding: 110px 0 120px 0;
  }
}


/* ---------------------------------- concept --> heading */

.cmn-head--teach-concept {
  margin-bottom: vw-sp(150);
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .cmn-head--teach-concept {
    margin-bottom: vw-pc(90);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-head--teach-concept {
    margin-bottom: 90px;
  }
}

/* ---------------------------------- component */

.what > li {
  position: relative;
  margin: 0 auto vw-sp(120) auto;
  width: vw-sp(650);
  background-color: $color-base;
}

.what > li:last-child {
  margin-bottom: 0;
}

.what-head {
  margin-bottom: 1em;
  color: $color-main;
  font-size: vw-sp(34);
  font-weight: 700;
  line-height: 1.6em;
}

@media screen and (min-width: $breakpoint1) {

  .what > li {
    margin-bottom: vw-pc(90);
    background: none;
    width: 100%;
    height: vw-pc(320);
    > div {
      position: absolute;
      top: 0;
      display: flex;
      justify-content: space-between;
      width: vw-pc(1370);
      height: 100%;
      background-color: $color-base;
    }
  }

  .what > li:nth-child(odd) > div {
    margin-left: vw-pc(30);
    padding-right: vw-pc(120);
    left: 0;
  }

  .what > li:nth-child(even) > div{
    margin-right: vw-pc(30);
    padding-left: vw-pc(200);
    right: 0;
  }

  .what-head {
    font-size: vw-pc(24);
  }
}

@media screen and (min-width: $breakpoint2) {

  .what > li {
    margin: 0 auto 90px 0;
    height: 320px;
    > div {
      width: 1370px;
    }
  }

  .what > li:nth-child(odd) > div {
    margin-left: 30px;
    padding-right: 120px;
  }

  .what > li:nth-child(even) > div{
    margin-right: 30px;
    padding-left: 200px;
  }

  .what-head {
    font-size: 24px; font-size: 2.4rem;
  }
}

.what-image {
  position: relative;
  width: vw-sp(560);
  z-index: 2;
}

.what-content {
  position: relative;
  z-index: 2;
}

@media screen and (max-width: $breakpoint1-max) {

  .what-image {
    margin: 0 auto vw-sp(-20) auto;
    top: vw-sp(-60);
  }

  .what-content {
    padding: 0 vw-sp(50) vw-sp(40) vw-sp(50);
  }
}

@media screen and (min-width: $breakpoint1) {

  .what-image {
    top: vw-pc(-30);
    width: vw-pc(480);
  }

  .what > li:nth-child(odd) .what-image {
    left: vw-pc(-30);
  }

  .what > li:nth-child(even) .what-image {
    right: vw-pc(-30);
    order: 2;
  }

  .what > li:nth-child(even) .what-content {
    order: 1;
  }

  .what-content {
    padding: vw-pc(70) 0;
    width: vw-pc(740);;
  }
}

@media screen and (min-width: $breakpoint2) {

  .what-image {
    top: -30px;
    width: 480px;
  }

  .what > li:nth-child(odd) .what-image {
    left: -30px;
  }

  .what > li:nth-child(even) .what-image {
    right: -30px;
  }

  .what-content {
    padding: 70px 0;
    width: 740px;
  }
}

/* ---------------------------------- component --> list */


.what-list li {
  position: relative;
  margin-bottom: .5em;
  padding-left: vw-sp(40);
  font-size: vw-sp(26);
  line-height: 1.8em;
}

.what-list li:last-child {
  position: relative;
  margin-bottom: 0;
}

.what-list li:before {
  content: '';
  position: absolute;
  top: .4em;
  left: 0;
  display: inline-block;
  width: vw-sp(29);
  height: vw-sp(29);
  background-image: url(~assets/img/common/check_b.png);
  background-size: contain;
  background-repeat: no-repeat;
}


@media screen and (min-width: $breakpoint1) {

  .what-list li {
    padding-left: vw-pc(30);
    font-size: vw-pc(16);
  }

  .what-list li:before {
    width: vw-pc(19);
    height: vw-pc(19);
  }
}

@media screen and (min-width: $breakpoint2) {

  .what-list li {
    padding-left: 30px;
    font-size: 16px; font-size: 1.6rem;
  }

  .what-list li:before {
    width: 19px;
    height: 19px;
  }
}

</style>
