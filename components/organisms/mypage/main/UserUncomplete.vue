<template>
      <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">未完了のテスト</h2>
        </div>
        <ul class="unfini">
          <li>
            <div class="unfini-header">
              <h3 class="mymain-subhead">長期コース - 機械学習の数学</h3>
              <p>0/100 点</p>
            </div>
            <div class="unfini-btns">
              <div class="mycmn-btn mycmn-btn--orange mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度学習する</span></a>
              </div>
              <div class="mycmn-btn mycmn-btn--blue mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度テストを受験する</span></a>
              </div>
            </div>
          </li>
          <li>
            <div class="unfini-header">
              <h3 class="mymain-subhead">長期コース - 機械学習の数学</h3>
              <p>0/100 点</p>
            </div>
            <div class="unfini-btns">
              <div class="mycmn-btn mycmn-btn--orange mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度学習する</span></a>
              </div>
              <div class="mycmn-btn mycmn-btn--blue mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度テストを受験する</span></a>
              </div>
            </div>
          </li>
          <li>
            <div class="unfini-header">
              <h3 class="mymain-subhead">長期コース - 機械学習の数学</h3>
              <p>0/100 点</p>
            </div>
            <div class="unfini-btns">
              <div class="mycmn-btn mycmn-btn--orange mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度学習する</span></a>
              </div>
              <div class="mycmn-btn mycmn-btn--blue mycmn-btn--low">
                <div></div>
                <a href="#"><span>再度テストを受験する</span></a>
              </div>
            </div>
          </li>
        </ul>
        <div class="display-btn"><p>すべてを表示する</p></div>
      </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ---------------------------------- unfini */

.unfini {
    margin-bottom: vw-sp(20);
}

.unfini li {
  margin-bottom: vw-sp(20);
  padding: vw-sp(35);
  background-color: $color-base;
}

.unfini li:last-child {
  margin-bottom: 0;
}

.unfini-header {
  margin-bottom: vw-sp(35);
  width: 100%;
}

.unfini-btns {
  display: flex;
  justify-content: space-between;
  width: 100%;
  > div {
    width: vw-sp(300);
  }
}

@media screen and (min-width: $breakpoint1) {

  .unfini {
    margin-bottom: vw-pc(10);
  }

  .unfini li {
    display: flex;
    justify-content: center;
    align-items: center;
    margin-bottom: vw-pc(10);
    padding: vw-pc(30);
  }

  .unfini-header {
    margin-bottom: 0;
    width: vw-pc(580);
  }

  .unfini-btns {
    width: vw-pc(530);
    > div {
      width: vw-pc(260);
    }
  }
}


</style>