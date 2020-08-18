<template>
    <section id="process" class="sec sec--teach-process">
      <div class="sec__in">
        <div class="cmn-head cmn-head--teach-process">
          <p class="cmn-head__en">process</p>
          <h2 class="cmn-head__jp">認定クリエイターとして<br class="br--sp">活躍するまでの5つのステップ</h2>
        </div>
        <div class="teach-process-box">
          <ul class="teach-process">
            <li>
              <div class="teach-process-circle">
                <div>
                  <div class="teach-process-icon">
                    <img src="~/assets/img/teach/process01.png" srcset="~/assets/img/teach/process01.png 1x,~/assets/img/teach/process01-2x.png 2x" class="img--fit" alt="STEP 01">
                  </div>
                  <p class="teach-process-num">STEP 01</p>
                </div>
              </div>
              <div class="teach-process-content">
                <h4 class="teach-process-head">応募</h4>
                <p>まずは、無料の申込みを行います。<br>申込時に簡単なテストを受験し、合格すると次のステップに進むことができます。</p>
              </div>
            </li>
            <li>
              <div class="teach-process-circle">
                <div>
                  <div class="teach-process-icon">
                    <img src="~/assets/img/teach/process02.png" srcset="~/assets/img/teach/process02.png 1x,~/assets/img/teach/process02-2x.png 2x" class="img--fit" alt="STEP 02">
                  </div>
                  <p class="teach-process-num">STEP 02</p>
                </div>
              </div>
              <div class="teach-process-content">
                <h4 class="teach-process-head">学習</h4>
                <p>認定クリエイターとして活躍するために必要となる、<br class="br--pc">エンジニアリングや資料作成などのスキルについて、ikusaiコンテンツを通して学びます。<br>学習のための費用は無料です。</p>
              </div>
            </li>
            <li>
              <div class="teach-process-circle">
                <div>
                  <div class="teach-process-icon">
                    <img src="~/assets/img/teach/process03.png" srcset="~/assets/img/teach/process03.png 1x,~/assets/img/teach/process03-2x.png 2x" class="img--fit" alt="STEP 03">
                  </div>
                  <p class="teach-process-num">STEP 03</p>
                </div>
              </div>
              <div class="teach-process-content">
                <h4 class="teach-process-head">認定</h4>
                <p>認定クリエイターとして必要最低限のスキルのテストを受験します。<br>テストは何度も受験することができ、合格すると認定クリエイターとしてデビューし、<br class="br--pc">動画講座の作成に取り組むことができるようになります。</p>
              </div>
            </li>
            <li>
              <div class="teach-process-circle">
                <div>
                  <div class="teach-process-icon">
                    <img src="~/assets/img/teach/process04.png" srcset="~/assets/img/teach/process04.png 1x,~/assets/img/teach/process04-2x.png 2x" class="img--fit" alt="STEP 04">
                  </div>
                  <p class="teach-process-num">STEP 04</p>
                </div>
              </div>
              <div class="teach-process-content">
                <h4 class="teach-process-head">講座作成</h4>
                <p>ikus.aiチームのプロデュース（監督）のもと、講座作成を行います。<br>講座作成が未経験でもクオリティ・ニーズの高い講座を作成するために、<br class="br--pc">徹底的にikus.aiチームメンバーがサポートします。</p>
              </div>
            </li>
            <li>
              <div class="teach-process-circle">
                <div>
                  <div class="teach-process-icon">
                    <img src="~/assets/img/teach/process05.png" srcset="~/assets/img/teach/process05.png 1x,~/assets/img/teach/process05-2x.png 2x" class="img--fit" alt="STEP 05">
                  </div>
                  <p class="teach-process-num">STEP 05</p>
                </div>
              </div>
              <div class="teach-process-content">
                <h4 class="teach-process-head">収益を得る</h4>
                <p>講座の売上に応じた収益を得ることができます。<br>講座は公開後ikus.aiのプラットフォーム上で公開され、継続的に収益を得ることができます。</p>
              </div>
            </li>
          </ul>
          <div class="teach-process-illust01">
            <img src="~/assets/img/teach/illust01.png" srcset="~/assets/img/teach/illust01.png 1x,~/assets/img/teach/illust01-2x.png 2x" class="img--fit" alt="illust">
          </div>
          <div class="teach-process-illust02">
            <img src="~/assets/img/teach/illust02.png" srcset="~/assets/img/teach/illust02.png 1x,~/assets/img/teach/illust02-2x.png 2x" class="img--fit" alt="illust">
          </div>
          <div class="teach-process-illust03">
            <img src="~/assets/img/teach/illust03.png" srcset="~/assets/img/teach/illust03.png 1x,~/assets/img/teach/illust03-2x.png 2x" class="img--fit" alt="illust">
          </div>
        </div>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- process --> section */

.sec--teach-process {
  padding: vw-sp(120) 0;
  background-image: url(~assets/img/teach/process-bg.jpg);
  background-size: cover;
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-process {
    padding: vw-pc(110) 0 vw-pc(120) 0;;
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-process {
    padding: 110px 0 120px 0;
  }
}


/* ---------------------------------- process --> heading */

.cmn-head--teach-process {
  margin-bottom: vw-sp(80);
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .cmn-head--teach-process {
    margin-bottom: vw-pc(50);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-head--teach-process {
    margin-bottom: 50px;
  }
}


/* ---------------------------------- concept --> conponent */


.teach-process-box {
  position: relative;
  padding: vw-sp(50) vw-sp(30);
  width: 100%;
  background-color: $color-base;
  box-shadow: 0px 5px 30px 0px rgba(0, 0, 0, 0.2);
}

.teach-process {
  position: relative;
  width: 100%;
}

.teach-process li {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: vw-sp(50);
  z-index: 2;
}

.teach-process li:after {
  content: '';
  position: absolute;
  top: 20%;
  left: vw-sp(100);
  width: vw-sp(15);
  height: 100%;
  background-color: #f8f8f8;
  transform: translateX(-50%);
  z-index: -1;
}

.teach-process li:last-child::after {
  content: none;
}

.teach-process-circle {
  display: flex;
  justify-content: center;
  align-items: center;
  width: vw-sp(200);
  height: vw-sp(200);
  background-color: #f8f8f8;
  border-radius: 50%;
  text-align: center;
  z-index: 2;
}

.teach-process-num {
  display: inline-block;
  margin-top: .5em;
  font-family: $font2;
  font-size: vw-sp(28);
  font-weight: 700;
  text-align: center;
  @include marker;
}

.teach-process-content {
  width: vw-sp(400);
  p {
    line-height: 1.8em;
  }
}

.teach-process-head {
  margin-bottom: .5em;
  font-size: vw-sp(34);
  font-weight: 700;
}

.teach-process li:nth-child(1) .teach-process-icon img {
  width: vw-sp(55);
}

.teach-process li:nth-child(2) .teach-process-icon img {
  width: vw-sp(75);
}

.teach-process li:nth-child(3) .teach-process-icon img {
  width: vw-sp(51);
}

.teach-process li:nth-child(4) .teach-process-icon img {
  width: vw-sp(64);
}

.teach-process li:nth-child(5) .teach-process-icon img {
  width: vw-sp(65);
}

.teach-process-illust01 {
  position: absolute;
  top: vw-sp(320);
  right: vw-sp(50);
  width: vw-sp(65);
}

.teach-process-illust02 {
  position: absolute;
  top: vw-sp(760);
  right: vw-sp(80);
  width: vw-sp(100);
}

.teach-process-illust03 {
  position: absolute;
  bottom: vw-sp(395);
  right: vw-sp(60);
  width: vw-sp(60);
}

@media screen and (min-width: $breakpoint1) {

  .teach-process-box {
    padding: vw-pc(60) vw-pc(80);
  }

  .teach-process li {
    align-items: center;
    margin-bottom: vw-pc(40);
  }

  .teach-process li:after {
    left: vw-pc(90);
    width: vw-pc(10);
  }

  .teach-process-circle {
    width: vw-pc(190);
    height: vw-pc(190);
  }

  .teach-process-num {
    margin-top: 1em;
    font-size: vw-pc(18);
  }

  .teach-process-content {
    width: vw-pc(905);
  }

  .teach-process-head {
    font-size: vw-pc(24);
  }

  .teach-process li:nth-child(1) .teach-process-icon img {
    width: vw-pc(55);
  }

  .teach-process li:nth-child(2) .teach-process-icon img {
    width: vw-pc(75);
  }

  .teach-process li:nth-child(3) .teach-process-icon img {
    width: vw-pc(51);
  }

  .teach-process li:nth-child(4) .teach-process-icon img {
    width: vw-pc(64);
  }

  .teach-process li:nth-child(5) .teach-process-icon img {
    width: vw-pc(65);
  }

  .teach-process-illust01 {
    top: vw-pc(83);
    right: vw-pc(60);
    width: vw-pc(95);
  }

  .teach-process-illust02 {
    top: vw-pc(460);
    right: vw-pc(113);
    width: vw-pc(158);
  }

  .teach-process-illust03 {
    bottom: vw-pc(205);
    right: vw-pc(75);
    width: vw-pc(87);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-process-box {
    padding: 60px 80px;
  }

  .teach-process li {
    margin-bottom: 40px;
  }

  .teach-process li:after {
    left: 90px;
    width: 10px;
  }

  .teach-process-circle {
    width: 180px;
    height: 180px;
  }

  .teach-process-num {
    font-size: 18px; font-size: 1.8rem;
  }

  .teach-process-content {
    width: 825px;
  }

  .teach-process-head {
    font-size: 24px; font-size: 2.4rem;
  }

  .teach-process li:nth-child(1) .teach-process-icon img {
    width: 55px;
  }

  .teach-process li:nth-child(2) .teach-process-icon img {
    width: 75px;
  }

  .teach-process li:nth-child(3) .teach-process-icon img {
    width: 51px;
  }

  .teach-process li:nth-child(4) .teach-process-icon img {
    width: 64px;
  }

  .teach-process li:nth-child(5) .teach-process-icon img {
    width: 65px;
  }

  .teach-process-illust01 {
    top: 83px;
    right: 60px;
    width: 95px;
  }

  .teach-process-illust02 {
    top: 460px;
    right: 113px;
    width: 158px;
  }

  .teach-process-illust03 {
    bottom: 165px;
    right: 75px;
    width: 87px;
  }
}
</style>
