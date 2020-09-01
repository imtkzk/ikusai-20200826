<template>
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
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    .navigation{
        font-weight: 700;
        max-height: vw-pc(500);
        overflow-y:scroll;
        width: 100%;
        max-width: vw-pc(400);
        border-top: solid vw-pc(3) #16325e;
        .navigation-title{
            padding: vw-pc(25);
            height: vw-pc(80);
            h3{
                font-weight: 700;
                font-size: vw-pc(18);
                font-family: $font2, $font1;
            }
        }
    }
    @media screen and (max-width: $breakpoint1-max) {
        .navigation{
            max-height: 100%;
            overflow-y:visible;
            max-width: 100%;
            border-top: solid vw-sp(3) #16325e;
            .navigation-title{
                padding: vw-sp(25);
                height: vw-sp(80);
                h3{
                    font-size: vw-sp(18);
                }
            }
        }
    }

    @media screen and (min-width: $breakpoint2) {
        .navigation{
            max-width: 400px;
            max-height: 500px;
            border-top: solid 3px #16325e;
            .navigation-title{
                padding: 25px;
                height: 80px;
                h3{
                    font-size: 18px;
                    font-size: 1.8rem;
                }
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
  font-size: vw-pc(18);
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
  font-size: vw-pc(18);
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
.learn-acod-ragarea{
  font-size: vw-pc(13);
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

    @media screen and (max-width: $breakpoint1-max) {
        .learn-acod-title {
        font-size: vw-sp(24);
        height: vw-sp(120);
        }
        .learn-acod-title::before{
        height: vw-sp(120);
        width: vw-sp(120);
        margin-right: vw-sp(20);
        }
        .learn-acod-title.is-active::before {
        height: vw-sp(120);
        width: vw-sp(120);
        margin-right: vw-sp(20);
        }
        .learn-course li {
        min-height: vw-sp(80);
        font-size: vw-sp(24);
        }
        .learn-course li:before {
        height: vw-sp(120);
        width: vw-sp(120);
        margin-right: vw-sp(20);
        }
        .learn-course li.current:before {
        height: vw-sp(120);
        width: vw-sp(120);
        margin-right: vw-sp(20);
        }
        .learn-acod .learn-acod-tagarea .learn-tags--time{
        margin-right: vw-sp(20);
        }
        .learn-acod-tagarea .learn-tags--time::before{
        top: vw-sp(3);
        height: vw-sp(20);
        width: vw-sp(20);
        margin-right: vw-sp(10);
        }
        .current .learn-acod-tagarea .learn-tags--time::before{
        top: vw-sp(3);
        height: vw-sp(20);
        width: vw-sp(20);
        margin-right: vw-sp(10);
        }
        .learn-course .learn-acod-tagarea .learn-tags--time::before{
        top: vw-sp(3);
        height: vw-sp(20);
        width: vw-sp(20);
        margin-right: vw-sp(10);
        }
        .learn-course li.current .learn-acod-tagarea .learn-tags--time::before{
        top: vw-sp(3);
        height: vw-sp(20);
        width: vw-sp(20);
        margin-right: vw-sp(10);
        }
        .current .learn-acod-tagarea .learn-tags--movie::before{
        top: vw-sp(3);
        height: vw-sp(20);
        width: vw-sp(20);
        margin-right: vw-sp(10);
        }
        .learn-acod-content.is-open li {
        height: vw-sp(120);
        }
    }
    @media screen and (min-width: $breakpoint2) {
        .learn-acod-title {
        font-size: 18px;
        font-size: 1.8rem;
        height: 80px;
        }
        .learn-acod-title::before{
        height: 80px;
        width: 80px;
        margin-right: 20px;
        }
        .learn-acod-title.is-active::before {
        height: 80px;
        width: 80px;
        margin-right: 20px;
        }
        .learn-course li {
        min-height: 80px;
        font-size: 18px;
        font-size: 1.8rem;
        }
        .learn-course li:before {
        height: 80px;
        width: 80px;
        margin-right: 20px;
        }
        .learn-course li.current:before {
        height: 80px;
        width: 80px;
        margin-right: 20px;
        }
        .learn-acod .learn-acod-tagarea .learn-tags--time{
        margin-right: 20px;
        }
        .learn-acod-tagarea .learn-tags--time::before{
        top: 3px;
        height: 20px;
        width: 20px;
        margin-right: 10px;
        }
        .current .learn-acod-tagarea .learn-tags--time::before{
        top: 3px;
        height: 20px;
        width: 20px;
        margin-right: 10px;
        }
        .learn-course .learn-acod-tagarea .learn-tags--time::before{
        top: 3px;
        height: 20px;
        width: 20px;
        margin-right: 10px;
        }
        .learn-course li.current .learn-acod-tagarea .learn-tags--time::before{
        top: 3px;
        height: 20px;
        width: 20px;
        margin-right: 10px;
        }
        .current .learn-acod-tagarea .learn-tags--movie::before{
        top: 3px;
        height: 20px;
        width: 20px;
        margin-right: 10px;
        }
        .learn-acod-content.is-open li {
        height: 80px;
        }
    }
</style>