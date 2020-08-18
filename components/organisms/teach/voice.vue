<template>
    <section id="voice" class="sec sec--teach-voice">
      <div class="sec__in">
        <div class="cmn-head cmn-head--teach-voice">
          <p class="cmn-head__en">voice</p>
          <h2 class="cmn-head__jp">認定クリエイターの声</h2>
        </div>
        <ul class="teach-voice">
          <li>
            <div class="teach-voice-fukidashi">
              <div>
                <p>正直スキルも高くないところから認定クリエイターに応募しました。しかし、ikus.aiのコンテンツを通して、技術に対しての知識、教えるスキルの両方をしっかり身につけることができ、価値のあるコンテンツが発信できるようになりました。<br>今後も新たな知識を学び、アウトプットしていきたいです。</p>
              </div>
            </div>
            <div class="teach-voice-contents">
              <div class="teach-voice-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="TARO YAMADA">
              </div>
              <div class="teach-voice-content">
                <h3 class="teach-voice-head">田中 太郎</h3>
                <p>学生</p>
              </div>
            </div>
          </li>
          <li>
            <div class="teach-voice-fukidashi">
              <div>
                <p>正直スキルも高くないところから認定クリエイターに応募しました。しかし、ikus.aiのコンテンツを通して、技術に対しての知識、教えるスキルの両方をしっかり身につけることができ、価値のあるコンテンツが発信できるようになりました。<br>今後も新たな知識を学び、アウトプットしていきたいです。</p>
              </div>
            </div>
            <div class="teach-voice-contents">
              <div class="teach-voice-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="TARO YAMADA">
              </div>
              <div class="teach-voice-content">
                <h3 class="teach-voice-head">田中 太郎</h3>
                <p>学生</p>
              </div>
            </div>
          </li>
          <li>
            <div class="teach-voice-fukidashi">
              <div>
                <p>正直スキルも高くないところから認定クリエイターに応募しました。しかし、ikus.aiのコンテンツを通して、技術に対しての知識、教えるスキルの両方をしっかり身につけることができ、価値のあるコンテンツが発信できるようになりました。<br>今後も新たな知識を学び、アウトプットしていきたいです。</p>
              </div>
            </div>
            <div class="teach-voice-contents">
              <div class="teach-voice-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="TARO YAMADA">
              </div>
              <div class="teach-voice-content">
                <h3 class="teach-voice-head">田中 太郎</h3>
                <p>学生</p>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- concept --> section */

.sec--teach-voice {
  padding: vw-sp(100) 0 vw-sp(80) 0;
  background-color: #e7f5f9;
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-voice {
    padding: vw-pc(75) 0 vw-pc(120) 0;;
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-voice {
    padding: 75px 0 120px 0;
  }
}


/* ---------------------------------- concept --> heading */

.cmn-head--teach-voice {
  margin-bottom: vw-sp(85);
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .cmn-head--teach-voice {
    margin-bottom: vw-pc(65);
  }
}

@media screen and (min-width: $breakpoint2) {

  .cmn-head--teach-voice {
    margin-bottom: 65px;
  }
}


/* ---------------------------------- concept --> conponent */

.teach-voice li {
  margin: 0 auto vw-sp(80) auto;
  padding: vw-sp(30);
  width: vw-sp(640);
  background-color: $color-base;
}

.teach-voice li:last-child {
  margin-bottom: 0;
}

.teach-voice-fukidashi {
  position: relative;
  margin-bottom: vw-sp(30);
  padding: 1em;
  background-color: #f8f8f8;
  border-radius: vw-sp(15);
  div {
    height: vw-sp(300);
    overflow-y: auto;
  }
  p {
    font-weight: 700;
    line-height: 1.8em;
  }
}

.teach-voice-fukidashi:after {
  content: '';
  position: absolute;
  top: 100%;
  left: vw-sp(85);
  width: 0;
  height: 0;
  border-style: solid;
  border-width: vw-sp(15) vw-sp(15) 0 vw-sp(15);
  border-color: #f8f8f8 transparent transparent transparent;
}

.teach-voice-contents {
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.teach-voice-image {
  width: vw-sp(200);
  img {
    border-radius: 50%;
  }
}

.teach-voice-content {
  width: vw-sp(350);
  p {
    line-height: 1.8em;
  }
}

.teach-voice-head {
  margin-bottom: .5em;
  font-size: 1.125em;
  font-weight: 700;
}

@media screen and (min-width: $breakpoint1) {

  .teach-voice {
    display: flex;
    justify-content: space-between
  }

  .teach-voice li {
    margin: 0;
    padding: vw-pc(20);
    width: vw-pc(410);
  }

  .teach-voice-fukidashi {
    margin-bottom: vw-pc(20);
    border-radius: vw-pc(10);
    div {
      height: vw-pc(210);
    }
  }

  .teach-voice-fukidashi:after {
    left: vw-pc(45);
    border-width: vw-pc(10) vw-pc(10) 0 vw-pc(10);
  }

  .teach-voice-image {
    width: vw-pc(112);
  }

  .teach-voice-content {
    width: vw-pc(205);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-voice li {
    padding: 20px;
    width: 380px;
  }

  .teach-voice-fukidashi {
    margin-bottom: 20px;
    border-radius: 10px;
    div {
      height: 210px;
    }
  }

  .teach-voice-fukidashi:after {
    left: 45px;
    border-width: 10px 10px 0 10px;
  }

  .teach-voice-image {
    width: 112px;
  }

  .teach-voice-content {
    width: 205px;
  }
}

</style>
