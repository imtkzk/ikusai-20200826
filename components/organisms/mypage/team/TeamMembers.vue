<template>
      <section>
        <div class="mymain-head-header">
          <h2 class="mymain-head">チームメンバー</h2>
        </div>
        <div class="team-mem-outer">
        <div class="team-mem">
          <swiper class="swiper-wrapper" :options="swiperOption">
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
            <swiper-slide class="swiper-slide team-mem-item">
              <div class="team-mem-image">
                <img src="~/assets/img/interview/image01.png" class="img--fit" alt="サンプル">
              </div>
              <h3 class="team-mem-name">Tanaka Taro</h3>
              <div class="team-mem-baloon">
                <p>はじめまして、よろしくお願いします！これから頑張っていきたいと思います！</p>
              </div>
            </swiper-slide>
          </swiper>
            <div id="example-slide-prev" class="team-mem-prev" slot="button-prev"></div>
            <div id="example-slide-next" class="team-mem-next" slot="button-next"></div>
        </div>
      </div>
      </section>
</template>

<script>
    export default {
        data() {
            return {
                swiperOption: {
                        loop: true,
                        loopAdditionalSlides: 1,
                        speed: 1500,
                        autoplay: {
                                delay: 2500,
                            },
                        slidesPerView: 2,
                        centeredSlides : true,
                        spaceBetween: 20,
                        navigation: {
                        nextEl: '.team-mem-next',
                        prevEl: '.team-mem-prev',
                        },
                        breakpoints: {
                        800: {
                            slidesPerView: 5,
                            spaceBetween: 20,
                        }
                    }
                }
            }
        }
    }
</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

    .swiper-container{
        overflow:visible;
    }

/* ---------------------------------- team-mem */

.team-mem-outer {
  position: relative;
  margin-left: vw-sp(-30);
  padding: 0 0 vw-sp(180) 0;
  width: vw-sp(750);
  position: relative;
  overflow-x: hidden;
}

.team-mem {
  margin: 0 auto;
  width: vw-sp(690);
}

.team-mem-item {
  position: relative;
  display: block;
  padding: vw-sp(35);
  border-radius: vw-sp(10);
  border: vw-sp(3) solid $color-base;
  background-color: $color-base;
  box-shadow: 0px 5px 15px 0px rgba(0, 0, 0, 0.2);
  text-align: center;
  transition: .3s;
}

.team-mem-item.swiper-slide-active {
  border: 2px solid $color-text;
}

.team-mem-image {
  margin: 0 auto 1em auto;
  width: vw-sp(220);
  img {
    border-radius: 50%;
  }
}

.team-mem-name {
  font-weight: 700;
  text-align: center;
}

.team-mem-baloon {
  position: absolute;
  top: vw-sp(400);
  left: 50%;
  padding: 1em;
  width: vw-sp(690);
  background-color: $color-text;
  border-radius: vw-sp(15);
  transform: translateX(-50%);
  visibility: hidden;
  opacity: 0;
  p {
    color: $color-base;
    font-weight: 700;
    line-height: 1.6em;
  }
}

.team-mem-baloon:before {
  content: '';
  position: absolute;
  bottom: 99%;
  left: 50%;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: 0 vw-sp(15) vw-sp(15) vw-sp(15);
  border-color: transparent transparent $color-text transparent;
  transform: translateX(-50%);

}

.team-mem-item.swiper-slide-active .team-mem-baloon {
  visibility: visible;
  opacity: 1;
}

@media screen and (min-width: $breakpoint1) {

  .team-mem-outer {
    margin-left: vw-pc(-60);
    padding: 0 0 vw-pc(90) 0;
    width: calc(100% + #{vw-pc(120)});
  }

  .team-mem {
    width: vw-pc(1080);
  }

  .team-mem-item {
    padding: vw-pc(25);
    border-radius: vw-pc(10);
    border: vw-pc(2) solid $color-base;
  }

  .team-mem-item.swiper-slide-active {
    border: vw-pc(2) solid $color-text;
  }

  .team-mem-image {
    width: vw-pc(120);
  }

  .team-mem-baloon {
    top: vw-pc(230);
    width: auto;
    border-radius: vw-pc(10);
    p {
      white-space: nowrap;
    }
  }

  .team-mem-baloon:before {
    border-width: 0 vw-pc(10) vw-pc(10) vw-pc(10);
  }
}


.team-mem-prev,
.team-mem-next {
  position: absolute;
  top: vw-sp(140);
  display: inline-block;
  width: vw-sp(70);
  height: vw-sp(70);
  background-size: contain;
  z-index: 888;
  transition: .3s;
}

.team-mem-prev:hover,
.team-mem-next:hover {
  opacity: 0.7;
}

.team-mem-prev {
  left: 85px;
  background-image: url(~assets/img/mypage/arrow-prev.png);
}

.team-mem-next {
  right: 85px;
  background-image: url(~assets/img/mypage/arrow-next.png);
}

@media screen and (min-width: $breakpoint1) {

  .special-head {
    font-size: vw-pc(120);
  }

  .team-mem-prev,
  .team-mem-next {
    top: vw-pc(75);
    width: vw-pc(50);
    height: vw-pc(50);
  }

  .team-mem-prev {
    left: vw-pc(85);
  }

  .team-mem-next {
    right: vw-pc(85);
  }
}


</style>
