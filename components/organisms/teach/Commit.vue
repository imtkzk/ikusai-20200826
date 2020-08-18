<template>
    <section id="commit" class="sec sec--teach-commit">
      <div class="sec__in">
          <h2 class="teach-commit-head">プロディースへのこだわり</h2>
          <div class="teach-commit">
            <div class="teach-commit-image">
              <img src="~/assets/img/teach/commit.png" srcset="~/assets/img/teach/commit.png 1x,~/assets/img/teach/commit-2x.png 2x" class="img--fit" alt="illust">
            </div>
            <div class="teach-commit-content">
              <p>正直スキルも高くないところから認定クリエイターに応募しました。<br>しかし、ikus.aiのコンテンツを通して、<br class="br--pc">技術に対しての知識、教えるスキルの両方をしっかり身につけることができ、<br class="br--pc">価値のあるコンテンツが発信できるようになりました。<br>今後も新たな知識を学び、アウトプットしていきたいです。</p>
            </div>
          </div>
      </div>
    </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- concept --> section */

.sec--teach-commit {
  padding: vw-sp(120) 0 vw-sp(110) 0;
  background-color: $color-base;
}

.sec--teach-commit:before {
  content: '';
  position: absolute;
  top: 50%;
  left: 50%;
  display: inline-block;
  width: vw-sp(350);
  height: vw-sp(418);
  background-image: url(~assets/img/teach/logo.png);
  background-size: contain;
  background-repeat: no-repeat;
  transform: translate(-50%, -50%);
}

@media screen and (min-width: $breakpoint1) {

  .sec--teach-commit {
    padding: vw-pc(125) 0 vw-pc(120) 0;;
  }

  .sec--teach-commit:before {
    width: vw-pc(295);
    height: vw-pc(352);
  }
}

@media screen and (min-width: $breakpoint2) {

  .sec--teach-commit {
    padding: 125px 0 120px 0;
  }

  .sec--teach-commit:before {
    width: 295px;
    height: 352px;
  }
}


/* ---------------------------------- concept --> heading */

.teach-commit-head {
  margin-bottom: 1em;
  font-size: vw-sp(40);
  font-weight: 700;
  text-align: center;
  line-height: 1.6em;
  letter-spacing: .2em;
}

@media screen and (min-width: $breakpoint1) {

  .teach-commit-head {
    margin-bottom: .5em;
    font-size: vw-pc(30);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-commit-head {
    font-size: 30px; font-size: 3.0rem;
  }
}


/* ---------------------------------- concept --> conponent */


.teach-commit {
  display: flex;
  justify-content: space-between;
  margin: 0 auto;
  width: 100%;
}

.teach-commit-image {
  align-self: flex-end;
  width: vw-sp(96);
}

.teach-commit-content {
  width: vw-sp(570);
  p {
    font-size: 1.125em;
    line-height: 1.8em;
  }
}

@media screen and (min-width: $breakpoint1) {

  .teach-commit {
    align-items: center;
    width: vw-pc(810);
  }

  .teach-commit-image {
    align-self: center;
    width: vw-pc(86);
  }

  .teach-commit-content {
    width: vw-pc(700);
  }
}

@media screen and (min-width: $breakpoint2) {

  .teach-commit {
    width: 810px;
  }

  .teach-commit-image {
    width: 86px;
  }

  .teach-commit-content {
    width: 700px;
  }
}

</style>
