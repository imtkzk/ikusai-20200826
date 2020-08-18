<template>
  <div id="signup-modal" class="modal">
    <div class="modal__in">
      <div id="signup-close" class="close-btn"><span></span></div>
      <h2 class="modal-head">新規登録（無料）して学習を始める</h2>
      <div class="form">
        <dl class="form-input form-input--user">
          <dt>ユーザー名</dt><dd><input type="text" placeholder="例）TANAKA TARO"></dd>
        </dl>
        <dl class="form-input form-input--mail">
          <dt>メールアドレス</dt><dd><input type="email" placeholder="例）taro.tanaka@gmail.com"></dd>
        </dl>
        <dl class="form-input form-input--password">
          <dt>パスワード</dt><dd><input type="password" placeholder="例）PassWord1234"></dd>
        </dl>
        <div class="form-consent form-consent--left">
          <label><input type="checkbox" name=""><span>ikus.ai からのオススメのコースや<br class="br--pc">お得な情報に関する<br class="br--sp">情報が掲載された案内メールを希望しない。</span></label>
        </div>
        <div class="form-btn">
          <SendForm>登録する</SendForm>
        </div>
        <p class="form-supply">新規登録すると、利用規約および<br class="br--sp">プライバシーポリシーに同意したとみなされます。</p>
        <div class="form-bottom">
          <p>すでにアカウントのお持ちの方は<span id="login-open02">ログイン</span></p>
        </div>
      </div>
    </div>
    <div id="signup-overlay" class="modal-overlay"></div>
  </div>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- common modal */

.modal {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  z-index: 9999;
  opacity: 0;
  visibility: hidden;
  transition: .6s;
}

.modal.is-show {
  opacity: 1;
  visibility: visible;
}

.modal__in {
  position: absolute;
  left: 50%;
  top: 50%;
  transform: translate(-50%,-50%);
  width: 100%;
  max-width: vw-sp(690);
  padding: vw-sp(90) vw-sp(40) vw-sp(60) vw-sp(40);
  background-color: $color-base;
  border-radius: vw-sp(15);
  z-index: 2;
}

.close-btn {
  position: absolute;
  right: vw-sp(25);
  top: vw-sp(25);
  text-align: center;
  cursor: pointer;
  transition: .3s;
}

.close-btn:before {
  content: '×';
  font-size: vw-sp(42);
  letter-spacing: 0;
}

.close-btn:hover {
  opacity: .7;
}

.modal-overlay {
  position: fixed;
  left: 0;
  top: 0;
  width: 100%;
  height: 100%;
  background-color: rgba(0,0,0,.6);
  z-index: 1;
  cursor: pointer;
}

.modal-head {
  margin-bottom: 2em;
  font-size: vw-sp(30);
  text-align: center;
  font-weight: 700;
  line-height: 1.5em;
  letter-spacing: .2em;
}

.modal-head--left {
  margin-bottom: 1em !important;
  text-align: left;
}

.modal-subhead {
  margin-bottom: 1em;
  font-weight: 700;
}

@media screen and (max-width: $breakpoint1-max) {

  .modal.is-show {
    height: 100vh;
    overflow-y: auto;
  }

  .modal.is-show .modal__in {
    top: 0;
    margin: vw-sp(50) 0;
    transform: translateX(-50%);
  }
}

@media screen and (min-width: $breakpoint1) {

  .modal__in {
    width: 80%;
    max-width: vw-pc(640);
    padding: vw-pc(55) vw-pc(60) vw-pc(50) vw-pc(60);
    border-radius: vw-pc(10);
  }

  .modal--large .modal__in {
    max-width: vw-pc(1100);
  }


  .close-btn {
    top: vw-pc(15);
    right: vw-pc(15);
  }

  .close-btn:before {
    font-size: vw-pc(32);
  }

  .modal-head {
    margin-bottom: 1.5em;
    font-size: vw-pc(24);
  }
}

@media screen and (min-width: $breakpoint2) {

  .modal__in {
    max-width: 600px;
    padding: 55px 60px 50px 60px;
    border-radius: 10px;
  }

  .modal--large .modal__in {
    max-width: 1000px;
  }

  .close-btn {
    top: 15px;
    right: 15px;
  }

  .close-btn:before {
    font-size: 32px; font-size: 3.2rem;
  }

  .modal-head {
    font-size: 24px; font-size: 2.4rem;
  }

}
/*  form
------------------------------------------------------------------------------*/

/* ---------------------------------- component --> form-input */

.form-input {
  margin-bottom: vw-sp(50);
}

.form-input dt {
  display: block;
  width: 100%;
  margin-bottom: .7em;
  font-weight: 700;
}

.form-input dd {
  position: relative;
  display: block;
  width: 100%;
}

.form-input dd:after {
  content: '';
  position: absolute;
  top: 50%;
  right: 1em;
  display: inline-block;
  background-size: contain;
  background-repeat: no-repeat;
  -webkit-transform: translateY(-50%);
  transform: translateY(-50%);
  z-index: 2;
}

.form-input--user dd:after {
  width: vw-sp(25);
  height: vw-sp(31);
  background-image: url(~assets/img/form/user.png);
}

.form-input--mail dd:after {
  width: vw-sp(27);
  height: vw-sp(22);
  background-image: url(~assets/img/form/mail.png);
}

.form-input--password dd:after {
  width: vw-sp(25);
  height: vw-sp(31);
  background-image: url(~assets/img/form/password.png);
}

.form-input--hint  dd:after {
  width: vw-sp(25);
  height: vw-sp(25);
  background-image: url(~assets/img/form/hint.png);
}

.form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"] {
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

  .form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"] {
    font-size: vw-pc(15);
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

  .form-input input[type="text"], .form-input input[type="email"], .form-input input[type="password"] {
    font-size: 15px;
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

/* ---------------------------------- component --> form-consent */

.form-consent {
  position: relative;
  margin: vw-sp(40) 0 vw-sp(35) 0;
  font-size: vw-sp(20);
  font-weight: 700;
  line-height: 1.5em;
  letter-spacing: .1em;
}

.form-consent--center {
  text-align: center;
}

.form-consent input[type="checkbox"] {
  display: none;
}

.form-consent input[type="checkbox"] + span {
  position: relative;
  display: inline-block;
  padding: 0 0 0 2em;
  cursor: pointer;
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

  .form-consent {
    margin: vw-pc(30) 0 vw-pc(25) 0;
    font-size: vw-pc(14);
  }

  .form input[type="checkbox"]:checked + span::after {
    border-left: vw-pc(3) solid $color-main;
    border-bottom: vw-pc(3) solid $color-main;
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-consent {
    margin: 30px 0 25px 0;
    font-size: 14px; font-size: 1.4rem;
  }

  .form input[type="checkbox"]:checked + span::after {
    border-left: 3px solid $color-main;
    border-bottom: 3px solid $color-main;
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


/* ---------------------------------- component --> form-supply */

.form-supply {
  margin-top: 1.5em;
  font-size: vw-sp(18);
  text-align: center;
  line-height: 1.5em;
}

@media screen and (min-width: $breakpoint1) {

  .form-supply {
    font-size: vw-pc(11);
    line-height: 2em;
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-supply {
    font-size: 11px; font-size: 1.1rem;
    line-height: 1.5em;
  }
}



/* ---------------------------------- component --> form-sns */

.form-sns {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin: vw-sp(50) auto;
  width: vw-sp(520);
}

.form-sns li {
  width: vw-sp(250);
  a {
    display: block;
  }
  a:hover {
    opacity: .7;
  }
}

@media screen and (min-width: $breakpoint1) {

  .form-sns {
    margin: vw-pc(40) auto;
    width: vw-pc(420);
  }

  .form-sns li {
    width: vw-pc(200);
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-sns {
    margin: 40px auto;
    width: 420px;
  }

  .form-sns li {
    width: 200px;
  }
}

/* ---------------------------------- component --> form-baloon */

.form-baloon {
  position: absolute;
  top: vw-sp(-85);
  left: 50%;
  padding: .5em;
  width: vw-sp(400);
  background-color: #d80000;
  border-radius: vw-sp(15);
  color: $color-base;
  font-size: vw-sp(18);
  font-weight: 700;
  text-align: center;
  line-height: 1.6em;
  transform: translateX(-50%);
  transition: .6s;
  visibility: hidden;
  opacity: 0;
}

.form-baloon:after {
  content: '';
  position: absolute;
  top: 98%;
  left: 50%;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: vw-sp(15) vw-sp(15) 0 vw-sp(15);
  border-color: #d80000 transparent transparent transparent;
  transform: translateX(-50%);
}

.form-input input[type="password"]:hover + .form-baloon,
.form-input input[type="password"]:focus + .form-baloon {
  visibility: visible;
  opacity: 1;
}

@media screen and (min-width: $breakpoint1) {

  .form-baloon {
    top: vw-pc(-65);
    width: vw-pc(320);
    border-radius: vw-pc(10);
    font-size: vw-pc(13);

  }

  .form-baloon:after {
    border-width: vw-pc(10) vw-pc(10) 0 vw-pc(10);
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-baloon {
    top: -65px;
    width: 280px;
    border-radius: 10px;
    font-size: 13px; font-size: 1.3rem;
  }

  .form-baloon:after {
    border-width: 10px 10px 0 10px;
  }
}


.form-baloon02 {
  position: absolute;
  top: vw-sp(-135);
  right: vw-sp(-35);
  padding: .5em;
  width: vw-sp(200);
  background-color: #16325e;
  border-radius: vw-sp(15);
  transition: .6s;
  visibility: hidden;
  opacity: 0;
}

.form-baloon02:after {
  content: '';
  position: absolute;
  top: 98%;
  left: 50%;
  width: 0;
  height: 0;
  border-style: solid;
  border-width: vw-sp(15) vw-sp(15) 0 vw-sp(15);
  border-color: #16325e transparent transparent transparent;
  transform: translateX(-50%);
}

.form-input input[type="text"]:hover + .form-baloon02,
.form-input input[type="text"]:focus + .form-baloon02 {
  visibility: visible;
  opacity: 1;
}

@media screen and (min-width: $breakpoint1) {

  .form-baloon02 {
    top: vw-pc(-65);
    right: vw-pc(-35);
    width: vw-pc(110);
    border-radius: vw-pc(10);

  }

  .form-baloon02:after {
    border-width: vw-pc(10) vw-pc(10) 0 vw-pc(10);
  }
}

@media screen and (min-width: $breakpoint2) {

  .form-baloon02 {
    top: -65px;
    right: -30px;
    width: 110px;
    border-radius: 10px;
  }

  .form-baloon02:after {
    border-width: 10px 10px 0 10px;
  }
}


/* ---------------------------------- component --> form-bottom */

.form-bottom {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: vw-sp(45) 0 0 0;
  padding: vw-sp(35) 0 0 0;
  border-top: vw-sp(3) solid $color-text;
  p {
    font-size: vw-sp(21);
    font-weight: 700;
    text-align: center;
  }
  span {
    display: inline-block;
    margin-left: 1em;
    padding-bottom: .5em;
    font-size: 1.23em;
    border-bottom: vw-sp(3) solid #a6acb9;
    transition: .3s;
  }

  span:hover {
    opacity: .7;
    cursor: pointer;
  }
}


@media screen and (min-width: $breakpoint1) {

  .form-bottom {
    margin: vw-pc(35) 0 0 0;
    padding: vw-pc(25) 0 0 0;
    border-top: vw-pc(2) solid $color-text;
    p {
      font-size: vw-pc(13);
    }

    span {
      border-bottom: vw-pc(2) solid #a6acb9;
    }
  }
}


@media screen and (min-width: $breakpoint2) {

  .form-bottom {
    margin: 35px 0 0 0;
    padding: 25px 0 0 0;
    border-top: 2px solid $color-text;
    p {
      font-size: 13px; font-size: 1.3rem;
    }

    span {
      border-bottom: 2px solid #a6acb9;
    }
  }
}

</style>
