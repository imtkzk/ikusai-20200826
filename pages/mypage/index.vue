<template>
    <div>
        <Header />
        <div class="container container--mypage">
            <main id="mymain" class="mymain">
                <div class="mymain-box">
                    <div class="mymain-box-member">
                        <UserProfileImage class="mymain-box-image" />
                    <!--<div class="mymain-box-graph">
                    <div><img src="~/assets/img/mypage/graph.png" class="img--fit" alt="graph"></div>
                    </div>-->
                    </div>
                </div>
                <UserLearning />
                <UserUncomplete />
                <RecommendedCourses>おすすめの他のコース</RecommendedCourses>
            </main>
            <Sidebar />
        </div>
        <editModal />
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import UserProfileImage from '~/components/organisms/mypage/UserProfileImage.vue'
    import UserLearning from '~/components/organisms/mypage/main/UserLearning.vue'
    import UserUncomplete from '~/components/organisms/mypage/main/UserUncomplete.vue'
    import RecommendedCourses from '~/components/organisms/mypage/main/RecommendedCourses.vue'
    import Sidebar from '~/layouts/Sidebar.vue'
    import editModal from '~/components/organisms/mypage/editModal.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            UserProfileImage,
            UserLearning,
            UserUncomplete,
            RecommendedCourses,
            Sidebar,
            editModal,
            Footer
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";



/*  dashboard
------------------------------------------------------------------------------*/

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


/* ---------------------------------- learn-box */

.learn-box {
  border: vw-sp(4) solid $color-main;
  background-color: #e9f9f2;
}

.learn-box-top {
  position: relative;
  display: flex;
  justify-content: space-between;
  margin-bottom: 0;
  padding: vw-sp(30) vw-sp(15) vw-sp(20) vw-sp(30);
  width: 100%;
  background-color: $color-base;
}

.learn-box-top:after {
  content: '';
  position: absolute;
  width: 0;
  height: 0;
  border-style: solid;
}

.learn-box-image {
  width: vw-sp(140);
}

.learn-box-content {
  width: vw-sp(470);
  p {
    line-height: 1.6em;
  }
}

.learn-box-name {
  font-size: 1.25em;
  font-weight: 700;
  text-align: center;
  line-height: 1.5em;
}

.learn-box-bottom {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  padding: vw-sp(60) vw-sp(40) vw-sp(40) vw-sp(40);
  width: 100%;
  height: 100%;
}

.learn-box-progress {
  margin-bottom: vw-sp(30);
  color: $color-orange;
  font-family: $font2,$font1;
  text-align: center;
  font-weight: 700;
  span {
    font-size: 1.5em;
  }
}

.learn-box-btn {
  margin: 0 auto;
  width: vw-sp(460);
}

@media screen and (max-width: $breakpoint1-max) {

  .learn-box-top:after {
    top: 100%;
    left: 0;
    border-width: 0 vw-sp(678) vw-sp(40) 0;
    border-color: transparent $color-base transparent transparent;
  }

}

@media screen and (min-width: $breakpoint1) {

  .learn-box {
    display: flex;
    justify-content: space-between;
    align-items: center;
    height: vw-pc(159);
    border: vw-pc(2) solid $color-main;
  }

  .learn-box-top {
    align-items: center;
    padding: vw-pc(30) vw-pc(15) vw-pc(30) vw-pc(30);
    width: vw-pc(810);
  }

  .learn-box-top:after {
    top: 0;
    left: 100%;
    border-width: vw-pc(155) vw-pc(40) 0 0;
    border-color: $color-base transparent transparent transparent;
  }

  .learn-box-image {
    width: vw-pc(142);
  }

  .learn-box-content {
    width: vw-pc(590);
  }

  .learn-box-bottom {
    padding: 0 vw-pc(30);
    width: vw-pc(360);
    height: 100%;
  }

  .learn-box-progress {
    margin-bottom: vw-pc(15);
  }

  .learn-box-btn {
    width: vw-pc(300);
  }
}

</style>
