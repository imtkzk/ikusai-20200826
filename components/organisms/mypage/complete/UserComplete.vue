<template>
    <div>
        <section>
            <div class="mymain-head-header">
            <h2 class="mymain-head">データサイエンス・機械学習</h2>
            </div>
            <ul class="skill-list">
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            </ul>
            <div class="display-btn"><p>すべてを表示する</p></div>
        </section>
        <section>
            <div class="mymain-head-header">
            <h2 class="mymain-head">フロントエンド</h2>
            </div>
            <ul class="skill-list">
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            </ul>
            <div class="display-btn"><p>すべてを表示する</p></div>
        </section>
        <section>
            <div class="mymain-head-header">
            <h2 class="mymain-head">バックエンド</h2>
            </div>
            <ul class="skill-list">
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            </ul>
            <div class="display-btn"><p>すべてを表示する</p></div>
        </section>
        <section>
            <div class="mymain-head-header">
            <h2 class="mymain-head">インフラストラクチャ</h2>
            </div>
            <div class="skill-none">
            <p>まだこの分野では習得したスキルがありません</p>
            </div>
            <div class="display-btn"><p>すべてを表示する</p></div>
        </section>
        <section>
            <div class="mymain-head-header">
            <h2 class="mymain-head">テスト</h2>
            </div>
            <ul class="skill-list">
            <li>機械学習の数学</li>
            <li>機械学習の数学</li>
            </ul>
            <div class="display-btn"><p>すべてを表示する</p></div>
        </section>
    </div>
</template>


<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ---------------------------------- skill-list */

.skill-list {
  display: flex;
  flex-wrap: wrap;
  margin-left: vw-sp(-20);
}

.skill-list li {
  position: relative;
  display: flex;
  align-items: center;
  margin: 0 0 vw-sp(20) vw-sp(20);
  padding-left: vw-sp(75);
  width: calc(50% - #{vw-sp(20)});
  height: vw-sp(80);
  background-color: $color-base;
  border: vw-sp(3) solid $color-main;
  font-size: 1em;
  font-weight: 700;
}

.skill-list li:before {
  content: '';
  position: absolute;
  top: 50%;
  left: vw-sp(27);
display: inline-block;
width: vw-sp(25);
height: vw-sp(32);
background-image: url(~assets/img/mypage/mark.png);
background-size: contain;
background-repeat: no-repeat;
transform: translateY(-50%);
}

@media screen and (min-width: $breakpoint1) {

  .skill-list {
    margin-left: vw-pc(-20);
  }

  .skill-list li {
    margin: 0 0 vw-pc(20) vw-pc(20);
    padding-left: vw-pc(75);
    width: calc(25% - #{vw-pc(20)});
    height: vw-pc(60);
    border: vw-pc(2) solid $color-main;
    font-size: 1.125em;
  }

  .skill-list li:before {
    left: vw-pc(17);
  width: vw-pc(20);
  height: vw-pc(26);
  }
}

.skill-none {
  margin-bottom: vw-sp(20);
  padding: 1.2em .5em;
  background-color: $color-base;
  font-size: 1em;
  font-weight: 700;
  line-height: 1.5em;
  text-align: center;
}

@media screen and (min-width: $breakpoint1) {

  .skill-none {
    margin-bottom: vw-pc(20);
    font-size: 1.125em;
  }
}
</style>