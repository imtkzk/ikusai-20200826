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
                    <UserComplete />
            </main>
            <Sidebar />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import UserProfileImage from '~/components/organisms/mypage/UserProfileImage.vue'
    import UserComplete from '~/components/organisms/mypage/complete/UserComplete.vue'
    import Sidebar from '~/layouts/Sidebar.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            UserProfileImage,
            UserComplete,
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
