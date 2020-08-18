<template>
    <div>
        <Header />
        <div class="container">
            <Hero />
            <PurchaseCard />
            <section id="detail" class="sec sec--detail">
                <div class="sec__in">
                    <ul class="detail">
                        <Skills />
                        <Target />
                        <Reason />
                        <Preknowledge />
                        <Environment />
                        <Contents />
                    </ul>
                </div>
            </section>
            <Campaign />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import Hero from '~/components/organisms/courseDetail/Hero.vue'
    import PurchaseCard from '~/components/organisms/courseDetail/PurchaseCard.vue'
    import Skills from '~/components/organisms/courseDetail/Skills.vue'
    import Target from '~/components/organisms/courseDetail/Target.vue'
    import Reason from '~/components/organisms/courseDetail/Reason.vue'
    import Preknowledge from '~/components/organisms/courseDetail/Preknowledge.vue'
    import Environment from '~/components/organisms/courseDetail/Environment.vue'
    import Contents from '~/components/organisms/courseDetail/Contents.vue'
    import Campaign from '~/components/organisms/top/Campaign.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            Hero,
            PurchaseCard,
            Skills,
            Target,
            Reason,
            Preknowledge,
            Environment,
            Contents,
            Campaign,
            Footer
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/scss/courseDetail.scss";
</style>
