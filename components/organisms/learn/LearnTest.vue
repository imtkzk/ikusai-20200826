<template>
    <div class="testInner">
        <div class="Qtitle"><span class="Qnum">1</span><h2>問題タイトルが入ります。</h2></div>
        <p class="testExplane">詳しい説明が入ります。</p>
        <div class="testImg">
            <img src="~/assets/img/common/sample.png">
        </div>
        <div class="testRequirements">
            <h3 class="RequirementsTitle"><span>要件</span></h3>
            <ul class="RequirementsList">
                <li>要件内容</li>
                <li>要件内容</li>
                <ul class="RequirementsList-inner">
                    <li>要件内容</li>
                    <li>要件内容</li>
                </ul>
                <li>要件内容</li>
                <li>要件内容</li>
            </ul>
        </div>
        <div class="testMath">
                    $$
                    y = wx + b
                    $$
        </div>
        <div class="testAnswer">
            <div class="form">
                <dl class="form-input">
                <dt><h3>回答</h3><p>複数選択式</p></dt>
                <dd>
                    <div class="testAnser-check">
                    <div><label><input type="checkbox" name="answer"><span>回答01</span></label></div>
                    <div><label><input type="checkbox" name="answer"><span>回答02</span></label></div>
                    <div><label><input type="checkbox" name="answer"><span>回答03</span></label></div>
                    </div>
                </dd>
                </dl>
                <div class="form-btn">
                    <SendForm>回答を送信</SendForm>
                </div>
            </div>
        </div>
        <div class="testAnswer">
            <div class="form">
                <dl class="form-input">
                <dt><h3>回答</h3><p>単一選択式</p></dt>
                <dd>
                    <div class="testAnser-type">
                    <div><label><input type="radio" name="answer"><span>回答01</span></label></div>
                    <div><label><input type="radio" name="answer"><span>回答02</span></label></div>
                    <div><label><input type="radio" name="answer"><span>回答03</span></label></div>
                    </div>
                </dd>
                </dl>
                <div class="form-btn">
                    <SendForm>回答を送信</SendForm>
                </div>
            </div>
        </div>
        <div class="testAnswer">
            <div class="form">
                <dl class="form-input">
                <dt><h3>回答</h3><p>テキスト入力</p></dt>
                <dd><textarea></textarea></dd>
                </dl>
                <div class="form-btn">
                    <SendForm>回答を送信</SendForm>
                </div>
            </div>
        </div>
        <div class="testAnswer">
            <div class="form">
                <dl class="form-input">
                <dt><h3>回答</h3><p>テキスト入力</p></dt>
                <dd><input type="file" name="testAnswer" value="testAnswer" class="input-file"></dd>
                </dl>
                <div class="form-btn">
                    <SendForm>回答を送信</SendForm>
                </div>
            </div>
        </div>
        <div class="testAnswer">
            <div class="form">
                <dl class="form-input">
                <dt><h3>回答</h3><p>画像単一選択式</p></dt>
                <dd>
                    <div class="testAnser-type--img">
                    <div><label><input type="radio" name="image" value="img" v-model="imageId">
            <span><img src="~/assets/img/common/sample.png"></span></label></div>
                    <div><label><input type="radio" name="image" value="img" v-model="imageId">
            <span><img src="~/assets/img/common/sample.png"></span></label></div>
                    <div><label><input type="radio" name="image" value="img" v-model="imageId">
            <span><img src="~/assets/img/common/sample.png"></span></label></div>
                    </div>
                </dd>
                </dl>
                <div class="form-btn">
                    <SendForm>回答を送信</SendForm>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
  head() {
    return {
      script: [
        {
          src: "https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.2/MathJax.js?config=TeX-AMS-MML_SVG"
        }
      ],
    };
  }
}
</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";
    @import "~assets/css/base.css";
    @import "~assets/css/codeblock.css";

    .testInner > div{
        margin:4em 0;
    }
    .testInner .testImg img{
        width: 100%;;
    }
    .testInner .testImg .testExplane{
        font-size: 18px;
        font-size: 1.8rem;
    }
    .Qtitle {
        display: flex;
        align-content: center;
        .Qnum{
        font-size: 24px;
        font-size: 2.4rem;
        font-weight: 700;
        line-height: 36px;
        font-family: "Montserrat", sans-serif, "Noto Sans JP", sans-serif;
        }
        .Qnum::before{
            content: "Q";
        }
        .Qnum::after{
            content: ".";
        }
        h2{
            margin: 0;
            font-size: 24px;
            font-size: 2.4rem;
            font-weight: 700;
            line-height: 36px;
            border-bottom:3px solid #16325e ;
        }
    }
    .testRequirements{
        background:#f8f8f8;
        padding: 2em;
        .RequirementsTitle{
            background: #16325e;
            padding: .5em 2em;
            display: inline-block;
            margin-bottom: 1em;
            span{
                font-size: 18px;
                font-size: 1.8rem;
                color:#fff;
                font-weight: 700;
            }
            span::before{
                content: "";
                display: inline-block;
                height: 1.125vw;
                width: 1.125vw;
                background-size: contain;
                background-repeat: no-repeat;
                background-image: url(~assets/img/learn/RequirementsTitle.png);
                margin-right: 0.625vw;
            }
        }
        .RequirementsList{
            padding-left: 2em;
            li{
                margin: 1em 0;
            }
            .RequirementsList-inner{
                padding-left: 2em;
            }
        }
    }
    .testAnswer{
        padding-bottom:2em;
    }
    .testAnswer .form .form-input{
        border:solid 3px $color-main;
        padding: 2em;
        margin-bottom: 3em;
    }

    /* ---------------------------------- component --> form-input */

.form-input {
  margin-bottom: vw-sp(50);
}

.form-input dt {
  display: flex;
  align-items: center;
  width: 100%;
  margin-bottom: 2em;
  font-weight: 700;
  h3{
      background: $color-main;
      color:$color-base;
      padding: .5em 2em;
      font-size: 24px;
      font-size: 2.4rem;
      font-weight: 700;
      margin: 0 1em 0 0;
  }
}

.form-input dd {
  position: relative;
  display: block;
  width: 100%;
}
.form-input dd div > div{
    margin-bottom: 2em;
}
.form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"], .form-input textarea, .form-input select {
  padding: 1em 1em;
  background-color: #f8f8f8;
  border: 1px solid $color-main;
  border-radius: .5em;
  width: 100%;
  color: $color-text;
  font-family: $font1;
  font-size: vw-sp(25);
  font-weight: 700;
  letter-spacing: .1em;
}
 .form-input textarea {
   height: vw-sp(24);
   line-height: 1.8em;
 }

.form-select {
  position: relative;
  width: vw-sp(300);
}

.form-select:after {
  content: '▼';
  position: absolute;
  top: 50%;
  right: .5em;
  color: $color-text;
  font-size: 0.875em;
  transform: translateY(-50%);
}

input::-webkit-input-placeholder,
select::-webkit-input-placeholder,
textarea::-webkit-input-placeholder {
  color: #dddfe2;
}
input:-ms-input-placeholder,
select:-ms-input-placeholder,
textarea:-ms-input-placeholder,
input::-ms-input-placeholder,
textarea::-ms-input-placeholder {
  color: #dddfe2;
}
input::-moz-placeholder,
select::-moz-placeholder,
textarea::-moz-placeholder {
  color: #dddfe2;
}

@media screen and (min-width: $breakpoint1) {

  .form-input {
    margin-bottom: vw-pc(25);
  }

  .form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"], .form-input textarea, .form-input select {
    font-size: vw-pc(15);
  }

  .form-input textarea {
    height: vw-pc(60);
  }

  .form-select {
    width: vw-pc(205);
  }

  .form-input--user dd:after {
    width: vw-pc(18);
    height: vw-pc(22);
  }

  .form-input--mail dd:after {
    width: vw-pc(20);
    height: vw-pc(16);
  }

  .form-input--password dd:after {
    width: vw-pc(18);
    height: vw-pc(22);
  }

  .form-input--hint  dd:after {
    width: vw-pc(20);
    height: vw-pc(20);
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-input {
    margin-bottom: 25px;
  }

  .form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"], .form-input textarea, .form-input select {
    font-size: 15px;
  }

  .form-input textarea {
    height: 200px;
  }

  .form-select {
    width: 205px;
  }

  .form-input--user dd:after {
    width: 18px;
    height: 22px;
  }

  .form-input--mail dd:after {
    width: 20px;
    height: 16px;
  }

  .form-input--password dd:after {
    width: 18px;
    height: 22px;
  }

  .form-input--hint  dd:after {
    width: 20px;
    height: 20px;
  }
}

/* ---------------------------------- component --> form-date */

.form-date label {
  margin-bottom: vw-sp(30);
}

.form-date label:last-child {
  margin-bottom: 0;
}

.form-date span {
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: vw-sp(30);
  padding: 0 vw-sp(50) 0 vw-sp(125);
  width: 100%;
  background-color: #e9f9f2;
  border-radius: .8em;
  height: vw-sp(110);
  font-size: vw-sp(28);
  font-weight: 700;
  cursor: pointer;
}

.form-date input[type="radio"]:checked + span {
  background-color: $color-main;
  color: $color-base;
}

.form-date input[type="radio"] {
  display: none;
}

.form-date input[type="radio"] + span::before {
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(50);
  display: block;
  width: vw-sp(50);
  height: vw-sp(50);
  background-color: $color-base;
  border-radius: 50%;
  transform: translateY(-50%);
}

.form-date input[type="radio"]:checked + span::after {
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(50);
  transform: translateY(-50%);
  background-color: $color-text;
  border-radius: 50%;
  width: vw-sp(30);
  height: vw-sp(30);
  border: vw-sp(10) solid $color-base;
  display: block;
}

@media screen and (min-width: $breakpoint1) {

  .form-date label {
    margin-bottom: vw-pc(20);
  }

  .form-date span {
    margin-bottom: vw-pc(20);
    padding: 0 vw-pc(50) 0 vw-pc(115);
    height: vw-pc(100);
    border-radius: 1em;
    font-size: vw-pc(18);
  }

  .form-date input[type="radio"] + span::before {
    left: vw-pc(50);
    width: vw-pc(40);
    height: vw-pc(40);
  }

  .form-date input[type="radio"]:checked + span::after {
    left: vw-pc(50);
    width: vw-pc(20);
    height: vw-pc(20);
    border: vw-pc(10) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-date label {
    margin-bottom: 20px;
  }

  .form-date span {
    margin-bottom: 20px;
    padding: 0 50px 0 115px;
    height: 100px;
    font-size: 18px; font-size: 1.8rem;
  }

  .form-date input[type="radio"] + span::before {
    left: 50px;
    width: 40px;
    height: 40px;
  }

  .form-date input[type="radio"]:checked + span::after {
    left: 50px;
    width: 20px;
    height: 20px;
    border: 10px solid $color-base;
  }
}

.form input[type="checkbox"] + span::before {
  position: absolute;
  content: '';
  top: 50%;
  left: 0;
  display: block;
  width: 1.3em;
  height: 1.3em;
  background-color: #f8f8f8;
  border: 1px solid $color-main;
  border-radius: 0;
  transform: translateY(-50%);
}

.form input[type="checkbox"]:checked + span::after {
  position: absolute;
  content: '';
  top: 50%;
  left: 0;
  display: block;
  width: 1.3em;
  height: .6em;
  margin-top: -.2em;
  border-left: vw-sp(5) solid $color-main;
  border-bottom: vw-sp(5) solid $color-main;
  transform: translateY(-50%) rotate(-45deg);
}


@media screen and (min-width: $breakpoint1) {

  .form input[type="checkbox"]:checked + span::after {
    border-left: vw-pc(3) solid $color-main;
    border-bottom: vw-pc(3) solid $color-main;
  }
}

@media screen and (min-width: $breakpoint2) {

  .form input[type="checkbox"]:checked + span::after {
    border-left: 3px solid $color-main;
    border-bottom: 3px solid $color-main;
  }
}
/* ---------------------------------- radio button */

.testAnser-type label{
  margin-bottom: vw-sp(20);
}

.testAnser-type label:last-child{
  margin-bottom: 0;
}

.testAnser-type span{
  position: relative;
  display: flex;
  align-items: center;
  padding: 0 vw-sp(50) 0 vw-sp(110);
  width: 100%;
  background-color: #e9f9f2;
  border-radius: .5em;
  height: vw-sp(90);
  font-size: vw-sp(28);
  font-weight: 700;
  cursor: pointer;
}

.testAnser-type span {
  padding: 0 vw-sp(20) 0 vw-sp(100);
}

.testAnser-type input[type="radio"]:checked + span{
  background-color: $color-main;
  color: $color-base;
}

.testAnser-type input[type="radio"]{
  display: none;
}

.testAnser-type input[type="radio"] + span::before{
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(30);
  display: block;
  width: vw-sp(50);
  height: vw-sp(50);
  background-color: $color-base;
  border-radius: 50%;
  transform: translateY(-50%);
}

.testAnser-type input[type="radio"]:checked + span::after{
  position: absolute;
  content: '';
  top: 50%;
  left: vw-sp(30);
  transform: translateY(-50%);
  background-color: $color-text;
  border-radius: 50%;
  width: vw-sp(30);
  height: vw-sp(30);
  border: vw-sp(10) solid $color-base;
  display: block;
}
.testAnser-type--img{
    display: flex;
    justify-content: space-around;
    
}
.testAnser-type--img > div{
    width: 30%;
}
.testAnser-type--img > div img{
    width: 100%;
}
@media screen and (min-width: $breakpoint1) {

  .testAnser-type label{
    margin-bottom: vw-pc(10);
  }

  .testAnser-type span{
    padding: 0 vw-pc(50) 0 vw-pc(75);
    height: vw-pc(60);
    border-radius: .5em;
    font-size: vw-pc(18);
  }

  .testAnser-type span {
    padding: 0 vw-pc(20) 0 vw-pc(60);
  }

  .testAnser-type input[type="radio"] + span::before{
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
  }

  .testAnser-type input[type="radio"]:checked + span::after{
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
    border: vw-pc(8) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  .testAnser-type label{
    margin-bottom: 10px;
  }

  .testAnser-type span{
    padding: 0 50px 0 75px;
    height: 60px;
    font-size: 18px; font-size: 1.8rem;
  }

  .testAnser-type span {
    padding: 0 20px 0 60px;
  }

  .testAnser-type input[type="radio"] + span::before{
    left: 20px;
    width: 32px;
    height: 32px;
  }

  .testAnser-type input[type="radio"]:checked + span::after{
    left: 20px;
    width: 16px;
    height: 16px;
    border: 8px solid $color-base;
  }
}
/* ---------------------------------- radio img button */

.testAnser-type--img label{
  margin-bottom: vw-sp(20);
}

.testAnser-type--img span{
  position: relative;
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  width: 100%;
  cursor: pointer;
}

.testAnser-type--img input[type="radio"]{
  display: none;
}

.testAnser-type--img input[type="radio"] + span::before{
  position: absolute;
  content: '';
  top: 20%;
  left: vw-sp(30);
  display: block;
  width: vw-sp(50);
  height: vw-sp(50);
  background-color: $color-base;
  border-radius: 50%;
  transform: translateY(-50%);
}

.testAnser-type--img input[type="radio"]:checked + span::after{
  position: absolute;
  content: '';
  top: 20%;
  left: vw-sp(30);
  transform: translateY(-50%);
  background-color: $color-text;
  border-radius: 50%;
  width: vw-sp(30);
  height: vw-sp(30);
  border: vw-sp(10) solid $color-base;
  display: block;
}
.testAnser-type--img input[type="radio"]:checked + span{
  border: 3px solid $color-text;
}
.testAnser-type--img--img{
    display: flex;
    justify-content: space-around;
    
}
.testAnser-type--img--img > div{
    width: 30%;
}
.testAnser-type--img--img > div img{
    width: 100%;
}
@media screen and (min-width: $breakpoint1) {

  .testAnser-type--img label{
    margin-bottom: vw-pc(10);
  }

  .testAnser-type--img input[type="radio"] + span::before{
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
  }

  .testAnser-type--img input[type="radio"]:checked + span::after{
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
    border: vw-pc(8) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  .testAnser-type--img label{
    margin-bottom: 10px;
  }

  .testAnser-type--img span{
    padding: 0 50px 0 75px;
    height: 60px;
    font-size: 18px; font-size: 1.8rem;
  }

  .testAnser-type--img span {
    padding: 0 20px 0 60px;
  }

  .testAnser-type--img input[type="radio"] + span::before{
    left: 20px;
    width: 32px;
    height: 32px;
  }

  .testAnser-type--img input[type="radio"]:checked + span::after{
    left: 20px;
    width: 16px;
    height: 16px;
    border: 8px solid $color-base;
  }
}

/* ---------------------------------- checkbox */

.testAnser-check label{
  margin-bottom: vw-sp(20);
}

.testAnser-check label:last-child{
  margin-bottom: 0;
}

.testAnser-check span{
  position: relative;
  display: flex;
  align-items: center;
  padding: 0 vw-sp(20) 0 vw-sp(100);
  width: 100%;
  background-color: #f8f8f8;
  border-radius: .5em;
  height: vw-sp(90);
  font-size: vw-sp(28);
  font-weight: 700;
  cursor: pointer;
}

.testAnser-check input[type="checkbox"] {
  display: none;
}

.testAnser-check input[type="checkbox"] + span::before {
  position: absolute;
  left: vw-sp(30);
}

.testAnser-check input[type="checkbox"]:checked + span::after {
  left: vw-sp(30);
}

@media screen and (min-width: $breakpoint1) {

  .testAnser-check label {
    margin-bottom: vw-pc(10);
  }

  .testAnser-check span {
    padding: 0 vw-pc(20) 0 vw-pc(60);
    height: vw-pc(60);
    border-radius: .5em;
    font-size: vw-pc(18);
  }

  .testAnser-check input[type="checkbox"] + span::before {
    left: vw-pc(20);
  }

  .testAnser-check input[type="checkbox"]:checked + span::after {
    left: vw-pc(20);
  }
}

@media screen and (min-width: $breakpoint2) {

  .testAnser-check label {
    margin-bottom: 10px;
  }

  .testAnser-check span {
    padding: 0 20px 0 60px;
    height: 60px;
    font-size: 18px; font-size: 1.8rem;
  }

  .testAnser-check input[type="checkbox"] + span::before {
    left: 20px;
  }

  .testAnser-check input[type="checkbox"]:checked + span::after {
    left: 20px;
  }
}

/* ---------------------------------- component --> form-btn */

.form-btn {
  margin: 0 auto;
  width: vw-sp(400);
  .cmn-btn {
    border: none !important;
  }
}

.form-submit-btn {
  display: block;
  width: 100%;
  height: 100%;
  color: $color-base;
  font-size: vw-sp(26);
  font-weight: 700;
  letter-spacing: .1em;
}

.form-submit-btn:hover {
  color: #ff9f01;
}

@media screen and (min-width: $breakpoint1) {

  .form-btn {
    width: vw-pc(260);
  }

  .form-submit-btn {
    font-size: vw-pc(16);
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-btn {
    width: 260px;
  }

  .form-submit-btn {
    font-size: 16px; font-size: 1.6rem;
  }
}
</style>