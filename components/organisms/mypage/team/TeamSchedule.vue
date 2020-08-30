<template>
      <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">スケジュール</h2>
        </div>
        <div class="schedule">
          <div>
            <p class="schedule-head">2020/10/01<span>[19:00 ~ 21:00]</span></p>
            <div class="schedule-btns">
              <a href="#" target="_blank"><span>Zoom</span> を開く</a>
              <a href="#" target="_blank"><span>Slack</span> を開く</a>
            </div>
          </div>
        </div>
      </section>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* --------------------------------- schedule */

.schedule {
  position: relative;
  padding: vw-sp(60) vw-sp(35);
  border: vw-sp(3) solid $color-main;
  background-image: url(~assets/img/mypage/bg.png);
  background-size: cover;
  background-position: center;
  text-align: center;
}

.schedule-head {
  position: relative;
  display: inline-flex;
  justify-content: space-between;
  align-items: center;
  padding-left: vw-sp(50);
  font-family: $font2,$font1;
  font-size: vw-sp(30);
  font-weight: 700;
  span {
    margin-left: 1em;
    font-size: 1.2em;
  }
}

.schedule-head:before {
  content: '';
  position: absolute;
  top: 50%;
  left: 0;
  display: inline-block;
  width: vw-sp(30);
  height: vw-sp(33);
  background-image: url(~assets/img/mypage/schedule.png);
  background-size: contain;
  background-repeat: no-repeat;
  transform: translateY(-50%);
}

.schedule-btns {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: vw-sp(35) auto 0 auto;
  width: 100%;
}

.schedule-btns a {
  display: flex;
  justify-content: center;
  align-items: center;
  width: vw-sp(290);
  height: vw-sp(74);
  border-radius: vw-sp(10);
  color: $color-base;
  font-size: 1.125em;
  font-weight: 700;
  span {
    margin-right: .2em;
  }
}

.schedule-btns a:nth-child(1) {
  border: vw-sp(3) solid #2d8cff;
  background-color: #2d8cff;
}

.schedule-btns a:nth-child(2) {
  border: vw-sp(3) solid #4a154b;
  background-color: #4a154b;
}

.schedule-btns a:hover {
  background-color: $color-base;
}

.schedule-btns a:nth-child(1):hover {
  color: #2d8cff;
}

.schedule-btns a:nth-child(2):hover {
  color: #4a154b;
}

@media screen and (min-width: $breakpoint1) {

  .schedule {
    display: flex;
    justify-content: center;
    align-items: center;
    padding: 0;
    height: vw-pc(230);
    border: vw-pc(2) solid $color-main;
    background-image: url(~assets/img/mypage/bg.png);
    background-size: cover;
    background-position: center;
    text-align: center;
  }

  .schedule-head {
    padding-left: vw-pc(40);
    font-size: vw-pc(20);
  }

  .schedule-head:before {
    width: vw-pc(24);
    height: vw-pc(26);
  }

  .schedule-btns {
    margin: vw-pc(25) auto 0 auto;
    width: vw-pc(610);
  }

  .schedule-btns a {
    width: vw-pc(290);
    height: vw-pc(56);
    border-radius: vw-pc(10);
  }

  .schedule-btns a:nth-child(1) {
    border: vw-pc(2) solid #2d8cff;
  }

  .schedule-btns a:nth-child(2) {
    border: vw-pc(2) solid #4a154b;
  }
}

</style>
