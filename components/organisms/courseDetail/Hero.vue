<template>
    <div class="detail-hero">
      <div class="detail-hero__in">
        <div class="detail-hero-content">
          <p class="detail-hero-catch">ディープラーニングの<br>数学とプログラミングを<br class="br--sp"><strong>0</strong>から学ぶ</p>
          <p class="detail-hero-label"><span>ディープラーニングハンズオンコース</span></p>
          <p class="detail-hero-desc">本コースでは、Python、機械学習、ウェブの基礎を学び、最終的には自作のWebアプリケーション開発まで取り組みます。初学者で一気通貫して技術を学びたい方にオススメのコースです。</p>
          <p class="detail-hero-data">20,000人が受講 / 最終更新日 2020/8/30</p>
        </div>
      </div>
    </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- hero */

.detail-hero {
  position: relative;
  display: flex;
  align-items: center;
  height: vw-sp(900);
  background-image: url(~assets/img/detail/hero.jpg);
  background-size: cover;
  background-position: right;
}

.detail-hero__in {
  position: relative;
  margin: 0 auto;
  padding-bottom: vw-sp(60);
  width: vw-sp(690);
}

.detail-hero-content {
  width: 100%;
}

@media screen and (min-width: $breakpoint1) {

  .detail-hero {
    height: vw-pc(450);
  }

  .detail-hero__in {
    padding: 0;
    width: vw-pc(1200);
  }

  .detail-hero-content {
    width: vw-pc(780);
  }
}

@media screen and (min-width: $breakpoint2) {

  .detail-hero {
    height: 450px;
  }

  .detail-hero__in {
    width: $max-width;
  }

  .detail-hero-content {
    width: 780px;
  }
}


.detail-hero-catch {
  margin-bottom: .5em;
  position: relative;
  color: $color-base;
  font-size: vw-sp(48);
  font-weight: 700;
  line-height: 1.6em;
  letter-spacing: .2em;
  white-space: nowrap;
}

.detail-hero-catch strong {
  margin-right: .1em;
  color: #f9ff49;
  font-size: 1.66em;
  font-style: italic;
}

.detail-hero-label {
  display: inline-block;
  margin-bottom: vw-sp(25);
  padding: .6em .5em;
  background-color: $color-text;
  color: $color-base;
  font-size: vw-sp(30);
  font-weight: 700;
  line-height: 1.6em;
  letter-spacing: .2em;
}

.detail-hero-desc {
  margin-bottom: 1em;
  color: $color-base;
  font-size: vw-sp(28);
  font-weight: 700;
  line-height: 1.8em;
}

.detail-hero-data {
  color: $color-base;
  font-size: vw-sp(23);
}

@media screen and (min-width: $breakpoint1) {


  .detail-hero-catch {
    font-size: vw-pc(36);
  }

  .detail-hero-label {
    margin-bottom: vw-pc(25);
    padding: .6em 1.2em;
    font-size: vw-pc(18);
  }

  .detail-hero-desc {
    font-size: vw-pc(18);
  }

  .detail-hero-data {
    font-size: vw-pc(13);
  }
}

@media screen and (min-width: $breakpoint2) {

  .detail-hero-catch {
    font-size: 36px; font-size: 3.6rem;
  }

  .detail-hero-label {
    margin-bottom: 25px;
    font-size: 18px; font-size: 1.8rem;
  }

  .detail-hero-desc {
    font-size: 18px; font-size: 1.8rem;
  }

  .detail-hero-data {
    font-size: 13px; font-size: 1.3rem;
  }
}
</style>