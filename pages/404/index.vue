<template>
    <div>
        <Header />
        <div class="container">
            <section id="notfound" class="sec sec--notfound">
                <div class="sec__in notfound">
                    <div class="img">
                        <img src="~/assets/img/404/notfound.png" srcset="~/assets/img/404/notfound.png 1x,~/assets/img/404/notfound-2x.png 2x" class="img--fit" alt="404notfound">
                    </div>
                    <div class="txt">
                        <h2 class="notfound-head">404 NOT FOUND</h2>
                        <p class="notfound-content">お探しのページは一時的にアクセスができない状況にあるか、<br class="br--pc">
                            移動もしくは削除された可能性があります。<br class="br--pc">
                            また、URL、ファイル名にタイプミスがないか<br class="br--pc">
                            再度ご確認ください。</p>
                            <div class="btn">
                                <BackBtn >ikus.ai トップページへ</BackBtn>
                            </div>
                    </div>
                </div>
            </section>
        </div>
        <Footer />
    </div>
</template>

<script>
    import Header from '~/components/organisms/common/Header.vue'
    import Footer from '~/components/organisms/common/Footer.vue'

    export default {
        components: {
            Header,
            Footer
        }
    }

</script>


<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    /* ---------------------------------- what --> section */

    .sec--notfound {
        padding: vw-sp(100) 0 vw-sp(100) 0;
    }

    .sec--notfound:before,
    .sec--notfound:after {
        content: '';
        position: absolute;
        top: 50%;
        display: inline-block;
        background-size: contain;
        background-repeat: no-repeat;
        transform: translateY(-50%);
        z-index: -1;
    }

    .sec--notfound:before {
        left: vw-sp(-80);
        width: vw-sp(308);
        height: vw-sp(750);
        background-image: url(~assets/img/bg/bg-left.png);
    }

    .sec--notfound:after {
        right: vw-sp(-80);
        width: vw-sp(330);
        height: vw-sp(726);
        background-image: url(~assets/img/bg/bg-right.png);
    }

    @media screen and (min-width: $breakpoint1) {

        .sec--notfound {
            padding: vw-pc(110) 0 vw-pc(120) 0;
        }

        .sec--notfound:before {
            left: 0;
            width: vw-pc(308);
            height: vw-pc(750);
        }

        .sec--notfound:after {
            right: 0;
            width: vw-pc(330);
            height: vw-pc(726);
        }
    }

    @media screen and (min-width: $breakpoint2) {

        .sec--notfound {
            padding: 110px 0 120px 0;
        }

        .sec--notfound:before {
            width: 308px;
            height: 750px;
        }

        .sec--notfound:after {
            width: 330px;
            height: 726px;
        }
    }

        .notfound {
            display: flex;
            justify-content:center
        }
    @media screen and (min-width: $breakpoint1) {

        .notfound {
            display: flex;
            justify-content:center
        }
    }

    @media screen and (min-width: $breakpoint2) {

        .notfound {
            display: flex;
            justify-content: center
        }
    }
    .notfound-head {
        margin-bottom: 1em;
        font-size: vw-sp(40);
        font-weight: 700;
        text-align: left;
        line-height: 1.6em;
        letter-spacing: .2em;
        font-family: "Montserrat", sans-serif;
    }
    @media screen and (min-width: $breakpoint1) {

        .notfound-head {
            margin-bottom: .5em;
            font-size: vw-pc(30);
        }
    }

    @media screen and (min-width: $breakpoint2) {

        .notfound-head {
            font-size: 30px; font-size: 3.0rem;
      }
    }

    .notfound-content {
        width: vw-sp(480);
        font-size: 1.18em;
        line-height: 1.8em;
        margin-bottom: 1.5em;
    }

    @media screen and (min-width: $breakpoint1) {

    .notfound-content {
        width: vw-pc(580);
        }
    }
    @media screen and (min-width: $breakpoint2) {
    .notfound-content {
        width: 580px;
     }
    }
    .notfound .img{
        margin-right: 1.5em;
    }
    .btn{
        width: vw-sp(434);
    }
    @media screen and (min-width: $breakpoint1) {
        .btn{
            width: vw-sp(217);
        }
    }
    @media screen and (min-width: $breakpoint2) {
        .btn{
            width: vw-sp(150);
        }
    }
</style>
