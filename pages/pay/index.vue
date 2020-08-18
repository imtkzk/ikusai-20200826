<template>
    <div>
        <Header />
        <div class="container">
            <Hero />
            <LarningStyle />
            <PayApply />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import Hero from '~/components/organisms/pay/Hero.vue'
    import LarningStyle from '~/components/organisms/pay/LarningStyle.vue'
    import PayApply from '~/components/organisms/pay/PayApply.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            Hero,
            LarningStyle,
            PayApply,
            Footer
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
</style>
