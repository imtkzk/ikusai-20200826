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
                <LearnContents />
            </div>
        </div>
        <Footer />
    </div>
</template>

<script>
    import LearnHeader from '~/components/organisms/common/LearnHeader.vue'
    import MovieContents from '~/components/organisms/learn/MovieContents.vue'
    import LearnDocument from '~/components/organisms/learn/LearnDocument.vue'
    import LearnTest from '~/components/organisms/learn/LearnTest.vue'
    import LearnContents from '~/components/organisms/learn/LearnContents.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            LearnHeader,
            MovieContents,
            LearnDocument,
            LearnTest,
            LearnContents,
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

</style>
