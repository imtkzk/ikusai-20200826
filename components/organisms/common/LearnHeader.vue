<template>
    <div>
        <header id="header" class="header">
            <div class="header-logo">
                <h1><a href="index.html" class="on--opa"><img src="~/assets/img/common/ikusai-logo.svg" class="img--fit" alt="ikus.ai"></a></h1>
            </div>
            <h2>ディープラーニングハンズオンコース</h2>
            <div id="navigation" class="header-navi">
                    <div class="evaluation-btn"><a href="#">このコースを評価する</a></div>
                    <div class="mypage-btn">
                        <div></div>
                        <a href="#"><span>マイページに戻る</span></a>
                    </div>
            </div>
            <div id="toggle" class="toggle">
                <span></span>
                <span></span>
                <span></span>
            </div>
        </header>
    </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

    .header-navi{
        padding-right: vw-pc(30);
    }

    .mypage-btn {
        position: relative;
        display: flex;
        justify-content: center;
        margin: 0 auto;
        width: vw-sp(400);
        max-width: 100%;
        height: vw-sp(90);
        border-radius: 2em;
        border: $color-main solid vw-s(3);
        box-shadow: 0px 6px 20px 0px rgba(0, 0, 0, 0.2);
        font-family: $font2, $font1;
        background-color: $color-base;
        text-align: center;
        overflow: hidden;
        cursor: pointer;
    }
    .mypage-btn a {
        position: relative;
        display: flex;
        justify-content: center;
        align-items: center;
        flex-wrap: wrap;
        padding: .5em 0;
        width: 100%;
        height: vw-sp(90);
        color: $color-main;
        font-size: vw-sp(28);
        font-weight: 700;
        text-decoration: none;
        transition: all .5s ease;
        z-index: 2;
    }
    .mypage-btn a:hover {
        color: $color-base;
    }
    .mypage-btn>div {
        position: absolute;
        top: 0;
        width: 100%;
        height: vw-sp(90);
        left: -100%;
        background-image: -moz-linear-gradient(0deg, rgb(41, 108, 0) 0%, rgb(104, 224, 159) 0%, rgb(36, 203, 112) 100%);
        background-image: -webkit-linear-gradient(0deg, rgb(41, 108, 0) 0%, rgb(104, 224, 159) 0%, rgb(36, 203, 112) 100%);
        transition: all .5s ease;
        z-index: 1;
    }
    .mypage-btn:hover>div {
        left: 0;
        height: 100%;
    }
    .mypage-btn span {
        display: block;
        width: 100%;
        font-size: vw-sp(20);
    }
    .mypage-btn span:nth-of-type(1) {
        margin-bottom: .5em;
    }
    @media screen and (min-width: $breakpoint1) {

        .mypage-btn {
            margin: 0;
            width: vw-pc(200);
            height: vw-pc(60);
        }

        .mypage-btn a {
            height: vw-pc(60);
            font-size: vw-pc(16);
        }

        .mypage-btn>div {
            height: vw-pc(60);
        }
    }
    @media screen and (min-width: $breakpoint2) {

        .mypage-btn {
            width: 200px;
            height: 60px;
            border: 3px solid $color-main;
        }

        .mypage-btn a {
            height: 60px;
            font-size: 16px;
            font-size: 1.6rem;
        }

        .mypage-btn>div {
            height: 60px;
        }
    }
    @media screen and (min-width: $breakpoint1) {

        .mypage-btn {
            border: vw-pc(3) solid $color-main;
        }

        .mypage-btn span {
            font-size: vw-pc(15);
        }

    }
    @media screen and (min-width: $breakpoint2) {

        .mypage-btn span {
            font-size: 16px;
            font-size: 1.6rem;
        }
    }
    .evaluation-btn{
        margin-right: vw-pc(20);
        font-weight: 600;
    }
    .evaluation-btn::before{
        content:"★";
        color: #cccccc;
        font-size: 24px;
        font-size: 2.4em;
        vertical-align: middle;
    }
    /*  header
------------------------------------------------------------------------------*/


    .header {
        position: fixed;
        top: 0;
        left: 0;
        display: flex;
        justify-content: space-between;
        align-items: center;
        width: 100%;
        height: vw-sp(150);
        /* ヘッダー高さ */
        background-color: rgba(255, 255, 255, 1);
        z-index: 10;
    }

    .header--white {
        background-color: $color-base;
    }

    .header-logo {
        position: relative;
        padding-left: 4vw;
        width: vw-sp(300);
        z-index: 999;
    }


    @media screen and (min-width: $breakpoint1) {
        .header {
            justify-content: space-between;
            height: vw-pc(100);
        }

        .header-logo {
            padding-left: vw-pc(30);
            width: vw-pc(200);
        }

        .header-navi {
            display: flex;
            justify-content: flex-end;
            align-items: center;
            padding-left: vw-pc(20);
            border-left: #b9c1ce solid vw-pc(3);
        }
    }

    @media screen and (min-width: $breakpoint2) {
        .header {
            height: 100px;
            /* ヘッダー高さ */
        }

        .header-logo {
            padding-left: 30px;
            width: 200px;
        }

        .header-navi {
            width: calc(100% - 280px);
        }
    }
    .header h2{
        font-weight: 600;
        font-size: vw-pc(24);
        letter-spacing: .2em;
    }


    /* ------------------------------------ グローバルナビ（SP） */
    @media screen and (max-width: $breakpoint1) {

        .header-navi__in {
            display: block;
            padding-top: vw-sp(30);
            height: calc(100vh - 16vw);
            overflow-y: scroll;
        }

        .navi-member {
            margin: 0 auto;
            width: vw-sp(650);
        }

        .navi {
            margin-bottom: vw-sp(60);
        }

        .navi>div {
            width: 100%;
            font-weight: 700;
            border-bottom: 1px dotted $color-base;
        }

        .navi>div>p {
            padding: 1.5em 2em;
            color: $color-base;
            font-size: vw-sp(25);
        }

        .navi>div>p span:nth-of-type(1) {
            margin-right: 1.5em;
        }

        .navi>div>p:hover {
            background-color: $color-text;
        }
    }


    /* ----------------- トグルボタン - */

    .toggle {
        position: fixed;
        top: vw-sp(20);
        right: vw-sp(15);
        width: vw-sp(120);
        height: vw-sp(110);
        cursor: pointer;
        z-index: 555;
        transition: opacity 0.25s ease;
    }

    .toggle span {
        position: absolute;
        left: vw-sp(20);
        width: vw-sp(80);
        height: vw-sp(6);
        background-color: $color-text;
        -webkit-transition: all 0.35s ease;
        transition: all 0.35s ease;
        cursor: pointer;
    }

    .toggle span:nth-of-type(1) {
        top: vw-sp(24);
    }

    .toggle span:nth-of-type(2) {
        top: vw-sp(52);
    }

    .toggle span:nth-of-type(3) {
        top: vw-sp(80);
    }

    .toggle.is-active span:nth-of-type(1) {
        top: vw-sp(52); // 2番目のtopと同一値に
        -webkit-transform: rotate(45deg);
        transform: rotate(45deg);
    }

    .toggle.is-active span:nth-of-type(2) {
        display: none;
    }

    .toggle.is-active span:nth-of-type(3) {
        top: vw-sp(52); // 2番目のtopと同一値に
        -webkit-transform: rotate(-45deg);
        transform: rotate(-45deg);
    }

    @media screen and (min-width: $breakpoint1) {
        .toggle {
            display: none;
        }
    }




</style>
