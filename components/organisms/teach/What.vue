<template>
    <section id="what" class="sec sec--teach-what">
      <div class="sec__in">
        <div class="cmn-head cmn-head--teach-what">
          <p class="cmn-head__en">WHAT</p>
          <h2 class="cmn-head__jp">認定クリエイターでできること</h2>
        </div>
        <ul class="teach-what">
          <li>
            <div class="teach-what-image">
              <img src="~/assets/img/teach/what01.jpg" srcset="~/assets/img/teach/what01.jpg 1x,~/assets/img/teach/what01-2x.jpg 2x" class="img--fit" alt="無料で学べる">
            </div>
            <div class="teach-what-content">
              <h3 class="teach-what-head">無料で学べる</h3>
              <p>認定クリエイター候補になるとikus.ai上に公開されているコースを無料もしくは割引を受けて受講することができます。</p>
            </div>
          </li>
          <li>
            <div class="teach-what-image">
              <img src="~/assets/img/teach/what02.jpg" srcset="~/assets/img/teach/what02.jpg 1x,~/assets/img/teach/what02-2x.jpg 2x" class="img--fit" alt="動画講座を販売">
            </div>
            <div class="teach-what-content">
              <h3 class="teach-what-head">動画講座を販売</h3>
              <p>コースを公開し（無料）、売上に応じて、収益を得ることができます。</p>
            </div>
          </li>
          <li>
            <div class="teach-what-image">
              <img src="~/assets/img/teach/what03.jpg" srcset="~/assets/img/teach/what03.jpg 1x,~/assets/img/teach/what03-2x.jpg 2x" class="img--fit" alt="仲間ができる">
            </div>
            <div class="teach-what-content">
              <h3 class="teach-what-head">仲間ができる</h3>
              <p>コース作成は個人で行うのではなく、チームで行います。様々なスキルを持った仲間と出会うことができ、あなたのネットワークを広げることができます。</p>
            </div>
          </li>
        </ul>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- what --> section */

.sec--teach-what {
  padding: vw-sp(100) 0 vw-sp(100) 0;
}

.sec--teach-what:before,
.sec--teach-what:after {
  content: '';
  position: absolute;
  top: 50%;
  display: inline-block;
  background-size: contain;
  background-repeat: no-repeat;
  transform: translateY(-50%);
  z-index: -1;
}

.sec--teach-what:before {
  left: vw-sp(-80);
  width: vw-sp(308);
  height: vw-sp(750);
  background-image: url(~assets/img/bg/bg-left.png);
}

.sec--teach-what:after {
  right: vw-sp(-80);
  width: vw-sp(330);
  height: vw-sp(726);
  background-image: url(~assets/img/bg/bg-right.png);
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-what {
    padding: vw-pc(110) 0 vw-pc(120) 0;;
  }

  .sec--teach-what:before {
    left: 0;
    width: vw-pc(308);
    height: vw-pc(750);
  }

  .sec--teach-what:after {
    right: 0;
    width: vw-pc(330);
    height: vw-pc(726);
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-what {
    padding: 110px 0 120px 0;
  }

  .sec--teach-what:before {
    width: 308px;
    height: 750px;
  }

  .sec--teach-what:after {
    width: 330px;
    height: 726px;
  }
}


/* ---------------------------------- what --> heading */

.cmn-head--teach-what {
  margin-bottom: vw-sp(80);
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .cmn-head--teach-what {
    margin-bottom: vw-pc(90);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-head--teach-what {
    margin-bottom: 90px;
  }
}


/* ---------------------------------- what --> conponent */


.teach-what li {
  margin: 0 auto vw-sp(60) auto;
  width: vw-sp(640);
  border: vw-sp(3) solid $color-text;
}

.teach-what li:last-child {
  margin-bottom: 0;
}

.teach-what-content {
  padding: vw-sp(30) vw-sp(30) vw-sp(35) vw-sp(30);
  p {
    line-height: 1.8em;
  }
}

.teach-what-head {
  margin-bottom: .7em;
  font-size: vw-sp(34);
  font-weight: 700;
  text-align: center;
  line-height: 1.6em;
}


@media screen and (min-width: $breakpoint1) {

  .teach-what {
    display: flex;
    justify-content: space-between
  }

  .teach-what li {
    margin: 0;
    width: vw-pc(380);
    border: vw-pc(2) solid $color-text;
  }

  .teach-what-content {
    padding: vw-pc(20) vw-pc(20) vw-pc(25) vw-pc(20);
  }

  .teach-what-head {
    font-size: vw-pc(24);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-what {
    display: flex;
    justify-content: space-between
  }

  .teach-what li {
    margin-bottom: 0;
    width: 380px;
    border: 2px solid $color-text;
  }

  .teach-what-content {
    padding: 20px 20px 25px 20px;
  }

  .teach-what-head {
    font-size: 24px; font-size: 2.4rem;
  }
}
</style>
