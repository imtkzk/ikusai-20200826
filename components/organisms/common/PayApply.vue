<template>
  <div id="payment-modal" class="modal modal--large">
    <div class="modal__in">
      <div id="payment-close" class="close-btn"><span></span></div>
      <div class="payment-modal">
        <div class="payment-modal-top">
          <h2 class="modal-head modal-head--left">支払い情報を入力する</h2>
          <p class="modal-subhead">ご利用可能なクレジットカード</p>
          <div class="payment-modal-credit">
            <img src="~/assets/img/common/credit.png" srcset="~/assets/img/common/credit.png 1x,~/assets/img/common/credit-2x.png 2x" class="img--fit" alt="ご利用可能なクレジットカード">
          </div>
          <div class="form">
            <dl class="form-input">
              <dt>カード名義</dt><dd><input type="text" placeholder="例）TANAKA TARO"></dd>
            </dl>
            <dl class="form-input form-input--password">
              <dt>カード番号</dt><dd><input type="text" placeholder="例）1234 1234 1234 1234"></dd>
            </dl>
            <div class="form-input-harf">
              <dl class="form-input">
                <dt>有効期限</dt><dd><input type="password" placeholder="例）MM/YY"></dd>
              </dl>
              <dl class="form-input  form-input--hint">
                <dt>セキュリティーコード (CVC)</dt>
                <dd><div><input type="text" placeholder="例）123"><div class="form-baloon02"><p><img src="~/assets/img/common/cvc.png" srcset="~/assets/img/common/cvc.png 1x,~/assets/img/common/cvc-2x.png 2x" class="img--fit" alt="セキュリティーコード (CVC)"></p></div></div></dd>
              </dl>
            </div>
            <div class="form-consent form-consent--left">
              <label><input type="checkbox" name=""><span>今後もこのカードを使う</span></label>
            </div>
          </div>
        </div>
        <div class="payment-modal-bottom">
          <div class="apply-step3-detail">
            <h5 class="apply-step3-detail-head">ディープラーニングハンズオンコース</h5>
            <dl class="apply-step3-prices">
              <dt><span>消費税（10%）</span></dt>
              <dd>¥100,000</dd>
              <dt><span>請求額（合計）</span></dt>
              <dd>¥110,000</dd>
            </dl>
            <div class="apply-step3-detail-content">
              <p>本コースはReスキル給付金の対象コースです。受講時と受講完了時にハローワークで手続きを行う必要があります。<br>給付金は最大￥70,00です。給付金は受講完了時に支払いが行われます。<br><a href="#">給付金の詳細に関してはこちら →</a></p>
              <p>支払いを完了することにより、これらのサービス規約に同意したものとみなされます。</p>
            </div>
            <div class="payment-modal-btn">
              <SendForm>今すぐ購入する</SendForm>
            </div>
          </div>
        </div>
      </div>
    </div>
    <div id="payment-overlay" class="modal-overlay"></div>
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


.payment-modal-top {
  margin-bottom: vw-sp(60);
  width: 100%;
}

.payment-modal-bottom {
  width: 100%;
}

.payment-modal-btn {
  margin: vw-sp(35) auto 0 auto;
  width: 100%;
  .cmn-btn {
    border: none !important;
  }
}

.form-consent--left {
  text-align: left;
}

.payment-modal .form-consent--left {
  margin: 0 !important;
}

.payment-modal-credit {
  margin-bottom: 2em;
  width: vw-sp(400);
}

@media screen and (max-width: $breakpoint1-max) {

  .payment-modal .form-consent--left {
    font-size: 1em;
  }
}

@media screen and (min-width: $breakpoint1) {

  .payment-modal {
    display: flex;
    justify-content: space-between;
  }

  .payment-modal-top {
    margin-bottom: 0;
    width: vw-pc(500);
  }

  .payment-modal-bottom {
    width: vw-pc(420);
  }

  .form-input-harf {
    display: flex;
    justify-content: space-between;
    dl {
      width: 48%;
    }
  }

  .payment-modal-btn {
    margin: vw-pc(25) auto 0 auto;
  }

  .payment-modal-credit {
    width: vw-pc(236);
  }
}

@media screen and (min-width: $breakpoint2) {

  .payment-modal-top {
    width: 500px;
  }

  .payment-modal-bottom {
    width: 320px;
  }

  .payment-modal-btn {
    margin: 25px auto 0 auto;
  }

  .payment-modal-credit {
    width: 236px;
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
/* ---------------------------------- component --> step3 */


.apply-step3 {
  margin-bottom: vw-sp(120);
}

.apply-step3-top {
  margin-bottom: vw-sp(60);
  width: 100%;
}

.apply-step3-bottom {
  width: 100%;
}


@media screen and (min-width: $breakpoint1) {

  .apply-step3 {
    display: flex;
    justify-content: space-between;
    margin-bottom: vw-pc(60);
  }

  .apply-step3-top {
    margin-bottom: 0;
    width: vw-pc(485);
  }

  .apply-step3-bottom {
    width: vw-pc(570);
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-step3 {
    margin-bottom: 60px;
  }

  .apply-step3-top {
    width: 485px;
  }

  .apply-step3-bottom {
    width: 470px;
  }
}

.apply-step3-head {
  margin-bottom: .7em;
  font-weight: 700;
}

.apply-step3-detail {
  padding: vw-sp(35) vw-sp(30);
  background-color: #f8f8f8;
  border-radius: vw-sp(15);
}

.apply-step3-detail-head {
  margin-bottom: .5em;
  font-size: vw-sp(30);
  font-weight: 700;
  line-height: 1.5em;
}

.apply-step3-prices {
  display: flex;
  justify-content: space-between;
  flex-wrap: wrap;
  margin-bottom: 1.2em;
  dt {
    display: flex;
    align-items: center;
    width: vw-sp(220);
    font-size: .81em;
    font-weight: 700;
    line-height: 1.6em;
    span:after {
      content: '：';
    }
  }
  dd {
    display: flex;
    justify-content: flex-end;
    align-items: center;
    width: calc(100% - #{vw-sp(220)});
    font-family: $font2;
    font-size: 1.25em;
    font-weight: 700;
    line-height: 1.6em;
  }
}

.apply-step3-detail-content {
  padding-top: 1.5em;
  border-top: vw-sp(3) solid $color-text;
}

.apply-step3-detail-content p {
  margin-bottom: 1.5em;
  font-size: .81em;
  line-height: 1.8em;
  a {
    display: inline-block;
    padding-bottom: .3em;
    border-bottom: 1px solid $color-text;
  }
  a:hover {
    opacity: .7;
  }
}

.apply-step3-detail-content p:last-child {
  margin-bottom: 0;
}

.apply-step3-bottom > div {
  margin-bottom: vw-sp(50);
}

.apply-step3-bottom > div:last-child {
  margin-bottom: 0;
}

.pay-apply-type {
  display: flex;
  justify-content: space-between;
  > div {
    width: vw-sp(300);
  }
}

@media screen and (min-width: $breakpoint1) {

  .apply-step3-detail {
    padding: vw-pc(25) vw-pc(30);
    border-radius: vw-pc(10);
  }

  .apply-step3-detail-head {
    font-size: vw-pc(20);
  }

  .apply-step3-prices {
    dt {
      width: 50%;
    }
    dd {
      width: 50%;
    }
  }

  .apply-step3-detail-content {
    border-top: vw-pc(2) solid $color-text;
  }

  .apply-step3-bottom > div {
    margin-bottom: vw-pc(40);
  }

  .pay-apply-type {
    > div {
      width: vw-pc(275);
    }
  }
}

@media screen and (min-width: $breakpoint2) {

  .apply-step3-detail {
    padding: 25px 30px;
    border-radius: 10px;
  }

  .apply-step3-detail-head {
    font-size: 20px; font-size: 2.0rem;
  }

  .apply-step3-detail-content {
    border-top: 2px solid $color-text;
  }

  .apply-step3-bottom > div {
    margin-bottom: 40px;
  }

  .pay-apply-type {
    > div {
      width: 225px;
    }
  }
}


.pay-apply-type label {
  margin-bottom: vw-sp(20);
}

.pay-apply-type label:last-child {
  margin-bottom: 0;
}

.pay-apply-type span {
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

.pay-apply-type input[type="radio"]:checked + span {
  background-color: $color-main;
  color: $color-base;
}

.pay-apply-type input[type="radio"] {
  display: none;
}

.pay-apply-type input[type="radio"] + span::before {
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

.pay-apply-type input[type="radio"]:checked + span::after {
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

@media screen and (min-width: $breakpoint1) {

  .pay-apply-type label {
    margin-bottom: vw-pc(10);
  }

  .pay-apply-type span {
    padding: 0 vw-pc(50) 0 vw-pc(75);
    height: vw-pc(60);
    border-radius: .5em;
    font-size: vw-pc(18);
  }

  .pay-apply-type input[type="radio"] + span::before {
    left: vw-pc(20);
    width: vw-pc(32);
    height: vw-pc(32);
  }

  .pay-apply-type input[type="radio"]:checked + span::after {
    left: vw-pc(20);
    width: vw-pc(16);
    height: vw-pc(16);
    border: vw-pc(8) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-apply-type label {
    margin-bottom: 10px;
  }

  .pay-apply-type span {
    padding: 0 50px 0 75px;
    height: 60px;
    font-size: 18px; font-size: 1.8rem;
  }

  .pay-apply-type input[type="radio"] + span::before {
    left: 20px;
    width: 32px;
    height: 32px;
  }

  .pay-apply-type input[type="radio"]:checked + span::after {
    left: 20px;
    width: 16px;
    height: 16px;
    border: 8px solid $color-base;
  }
}


</style>

