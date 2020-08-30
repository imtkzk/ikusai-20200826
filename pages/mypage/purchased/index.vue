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
                <div class="mypage-apply">
                    <TopCTABtn />
                </div>
                <div class="mymain-head-header">
                    <div class="mymain-head-baloon">
                        <p>コースを受講し、学習を始めましょう！</p>
                    </div>
                </div>
                <RecommendedCourses>おすすめのコース</RecommendedCourses>
            </main>
            <Sidebar />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import UserProfileImage from '~/components/organisms/mypage/UserProfileImage.vue'
    import TopCTABtn from '~/components/atoms/top/TopCTABtn.vue'
    import RecommendedCourses from '~/components/organisms/mypage/main/RecommendedCourses.vue'
    import Sidebar from '~/layouts/Sidebar.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            UserProfileImage,
            TopCTABtn,
            RecommendedCourses,
            Sidebar,
            Footer
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/mypage.scss";

/* ---------------------------------- mypage-apply */

.mypage-apply {
  margin: vw-sp(150) 0 vw-sp(220) 0;
}

@media screen and (min-width: $breakpoint1) {

  .mypage-apply {
    margin: vw-pc(100) 0 vw-pc(120) 0;
  }
}
</style>
