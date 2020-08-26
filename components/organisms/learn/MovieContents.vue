<template>
    <div class="movie-contents">
      <div class="movie">
          <video src="assets/img/learn/movie.mp4" controls></video>
      </div>
      <div class="navigation">
          <div class="navigation-title">
             <h3>LESSONS</h3>
          </div>
              <ul class="learn-acod">
                <li>
                  <h4 class="learn-acod-title"><span>イントロダクション<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></h4>
                  <div class="learn-acod-content">
                    <ul class="learn-course">
                      <li><span>平均、分散、標準偏差<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                      <li><span>線形代数<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                    </ul>
                  </div>
                </li>
                <li class="current">
                  <h4 class="learn-acod-title is-active"><span>機械学習の数学<div class="learn-acod-tagarea"><small class="learn-tags--time">80 min</small><small class="learn-tags--movie">2 videos</small></div></span></h4>
                  <div class="learn-acod-content is-open">
                    <ul class="learn-course">
                      <li class="current"><span>平均、分散、標準偏差<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                      <li><span>線形代数<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                    </ul>
                  </div>
                </li>
                <li>
                  <h4 class="learn-acod-title"><span>イントロダクション<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></h4>
                  <div class="learn-acod-content">
                    <ul class="learn-course">
                      <li><span>平均、分散、標準偏差<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                      <li><span>線形代数<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                    </ul>
                  </div>
                </li>
                <li>
                  <h4 class="learn-acod-title"><span>イントロダクション<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></h4>
                  <div class="learn-acod-content">
                    <ul class="learn-course">
                      <li><span>平均、分散、標準偏差<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                      <li><span>線形代数<div class="learn-acod-tagarea"><small class="learn-tags--time">40 min</small></div></span></li>
                    </ul>
                  </div>
                </li>
              </ul>
        </div>
      </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    .movie-contents{
        display: flex;
        justify-content: center;
    }
    .movie{
        width: 100%;
        max-width: vw-pc(1000);
    }
    .movie video{
        width: 100%;
    }
    .navigation{
        font-weight: 600;
        max-height: vw-pc(500);
        overflow-y:scroll;
        width: 100%;
        max-width: vw-pc(400);
        border-top: solid vw-pc(3) #16325e;
        .navigation-title{
            padding: vw-pc(25);
            height: vw-pc(80);
            h3{
                font-size: vw-pc(18);
                font-family: $font2, $font1;
            }
        }
    }


/* ---------------------------------- accordion */

.learn-acod > li {
  background-color: #f3f5f7;
}
.learn-acod .learn-acod-tagarea { 
    color: #a7adb9;
    .learn-tags--time{
        margin-right: vw-pc(10);
    }
}
.learn-acod .current .learn-acod-tagarea { 
    color: #a7e9c8;
}
.learn-acod .learn-acod-content { 
    color: $color-main;
    .learn-acod-tagarea{
    color: $color-main;
    }
}
.learn-acod .learn-acod-content .current .learn-acod-tagarea{ 
    color: #a7e9c8;
}

.learn-acod-title {
  position: relative;
  display: flex;
  align-items: center;
  height: vw-pc(80);
  font-weight: 700;
  line-height: 1.6em;
  cursor: pointer;
  user-select: none;
}

.learn-acod-title::before{
  content: '＋';
  line-height: 4.6em;
  font-weight: 700;
  position: relative;
  top: 50%;
  text-align: center;
  height: vw-pc(80);
  width: vw-pc(80);
  background-color: #f9fafb;
  transform: translateY(-50%);
  margin-right: vw-pc(20);
}

.learn-acod-title.is-active::before {
  content: 'ー';
  font-weight: 700;
  line-height: 4.6em;
  position: relative;
  top: 50%;
  text-align: center;
  height: vw-pc(80);
  width: vw-pc(80);
  background-color: #f9fafb;
  transform: translateY(-50%);
  margin-right: vw-pc(20);
}

.learn-acod-content {
  padding: 0;
  height: 0;
  opacity: 0;
  transition-duration: .3s;
}
.learn-acod-content li {
  height: 0;
  opacity: 0;
  transition-duration: .3s;
}

.learn-acod-content.is-open {
  line-height: normal;
  height: auto;
  opacity: 1;
}
.learn-acod-content.is-open li {
  height: vw-pc(80);
  opacity: 1;
}

.learn-course li {
  position: relative;
  display: flex;
  align-items: center;
  background-color: $color-base;
  min-height: vw-pc(80);
}

.learn-course li.current {
    background-color: #2ac584;
    color: $color-base;
}
.learn-course li:before {
  content: '';
  position: relative;
  top: 50%;
  left: 0;
  display: inline-block;
  height: vw-pc(80);
  width: vw-pc(80);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/before-movie.png);
  transform: translateY(-50%);
  margin-right: vw-pc(20);
}
.learn-course li.current:before {
  content: '';
  background-color: #95e2c2;
  position: relative;
  top: 50%;
  left: 0;
  display: inline-block;
  height: vw-pc(80);
  width: vw-pc(80);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/before-movie-current.png);
  transform: translateY(-50%);
  margin-right: vw-pc(20);
}
.current .learn-acod-title{
    background-color: #2ac584;
    color: $color-base;
}
.current .learn-acod-title::before{
    background-color: #95e2c2;
}
.learn-acod-tagarea .learn-tags--time::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--time.png);
  margin-right: vw-pc(10);
}
.learn-acod-tagarea .learn-tags--movie::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--movie.png);
  margin-right: vw-pc(10);
}
.current .learn-acod-tagarea .learn-tags--time::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--time-current.png);
  margin-right: vw-pc(10);
}
.learn-course .learn-acod-tagarea .learn-tags--time::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--time-li.png);
  margin-right: vw-pc(10);
}
.learn-course li.current .learn-acod-tagarea .learn-tags--time::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--time-current.png);
  margin-right: vw-pc(10);
}
.current .learn-acod-tagarea .learn-tags--movie::before{
  content: "";
  position: relative;
  top: vw-pc(6);
  display: inline-block;
  height: vw-pc(20);
  width: vw-pc(20);
  background-size: contain;
  background-repeat: no-repeat;
  background-image: url(~assets/img/learn/learn-tags--movie-current.png);
  margin-right: vw-pc(10);
}
</style>