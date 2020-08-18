<template>
    <div>
        <Header />
        <div class="container">
            <Hero />
            <Concept />
            <What />
            <Process />
            <Voice />
            <Commit />
            <Apply />
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import Hero from '~/components/organisms/teach/Hero.vue'
    import Concept from '~/components/organisms/teach/Concept.vue'
    import What from '~/components/organisms/teach/What.vue'
    import Process from '~/components/organisms/teach/Process.vue'
    import Voice from '~/components/organisms/teach/Voice.vue'
    import Commit from '~/components/organisms/teach/Commit.vue'
    import Apply from '~/components/organisms/teach/Apply.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            Hero,
            Concept,
            What,
            Process,
            Voice,
            Commit,
            Apply,
            Footer
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
</style>
