<template>
    <div>
        <LearnHeader />
        <div class="container">
            <MovieContents />
            <div class="content">
                <div class="tabs">
                        <input id="document" type="radio" name="tab_item" checked><label class="tab_item" for="document">資料</label>
                        <input id="test" type="radio" name="tab_item"><label class="tab_item" for="test">テスト</label>
                        <span class="line"></span>
                    <div class="tab_content" id="document_content">
                        <LearnDocument />
                    </div>
                    <div class="tab_content" id="test_content">
                        <LearnTest />
                    </div>
                </div>
                <LearnContents class="none--sp" />
            </div>
        </div>
        <MovieNavigation class="none--pc" />
        <LearnContents class="none--pc" />
        <Footer />
    </div>
</template>

<script>
    import LearnHeader from '~/components/organisms/common/LearnHeader.vue'
    import MovieContents from '~/components/organisms/learn/MovieContents.vue'
    import LearnDocument from '~/components/organisms/learn/LearnDocument.vue'
    import LearnTest from '~/components/organisms/learn/LearnTest.vue'
    import LearnContents from '~/components/organisms/learn/LearnContents.vue'
    import MovieNavigation from '~/components/organisms/learn/MovieNavigation.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            LearnHeader,
            MovieContents,
            LearnDocument,
            LearnTest,
            LearnContents,
            MovieNavigation,
            Footer
        },
        head: {
            bodyAttrs: {
            class: 'body-learnpage'
            }
        }
    }

</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    
    .content {
        display: flex;
        justify-content: center;
    }
    .tabs {
        background-color: #fff;
        width: vw-pc(1000);
    }
    @media screen and (max-width: $breakpoint1-max) {
        .tabs{
            width: calc(100% - 30px);
        }
    }
    @media screen and (min-width: $breakpoint2) {
        .tabs{
            width: 1000px;
        }
    }
    .line{
        width: 100%;
        height: 0.1875vw;
        display: block;
        background-color: #acb6c7;
        position: relative;
        top: vw-pc(80);
    }

    .tab_item {
        height: vw-pc(80);
        line-height: vw-pc(80);
        font-size: vw-pc(18);
        color: #acb6c7;
        display: block;
        float: left;
        text-align: center;
        font-weight: bold;
        transition: all 0.2s ease;
        padding: 0 vw-pc(30);
    }
    @media screen and (max-width: $breakpoint1-max) {
        .tab_item {
                height: vw-sp(80);
                line-height: vw-sp(80);
                font-size: vw-sp(18);
                padding: 0 vw-sp(30);
        }
        .line{
                top: vw-sp(80);
        }
    }
    @media screen and (min-width: $breakpoint2) {
        .tab_item {
                height: 80px;
                line-height: 80px;
                font-size: 18px;
                font-size: 1.8rem;
                padding: 0 30px;
        }
        .line{
                top: 80px;
        }
    }
    .tab_item:hover {
        opacity: 0.75;
    }

    input[name="tab_item"] {
        display: none;
    }

    .tab_content {
        display: none;
        clear: both;
        overflow: hidden;
    }
    #document:checked~#document_content,
    #test:checked~#test_content{
        display: block;
    }

    .tabs input:checked+.tab_item {
        color: #16325e;
        border-bottom: vw-pc(8) solid #16325e;
    }
    @media screen and (max-width: $breakpoint1-max) {
    .tabs input:checked+.tab_item {
        border-bottom: vw-sp(8) solid #16325e;
    }
    }
    @media screen and (min-width: $breakpoint2) {
    .tabs input:checked+.tab_item {
        border-bottom: 8px solid #16325e;
    }
    }
</style>
