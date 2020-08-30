<template>
    <div>
        <Header />
        <div class="container container--mypage">
            <main id="mymain" class="mymain">
                <TeamSchedule />
                <TeamMembers />
                <TeamRules />
            </main>
            <SidebarTeam />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import TeamSchedule from '~/components/organisms/mypage/team/TeamSchedule.vue'
    import TeamMembers from '~/components/organisms/mypage/team/TeamMembers.vue'
    import TeamRules from '~/components/organisms/mypage/team/TeamRules.vue'
    import SidebarTeam from '~/layouts/SidebarTeam.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            TeamSchedule,
            TeamMembers,
            TeamRules,
            SidebarTeam,
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
