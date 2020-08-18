<template>
    <label><input type="radio" name="my-radio"><span><slot /></span></label>
</template>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";

/* ---------------------------------- component --> step1 --> apply-course */

label {
  margin-bottom: vw-sp(20);
}

label:last-child {
  margin-bottom: 0;
}

span {
  position: relative;
  display: flex;
  align-items: center;
  margin-bottom: vw-sp(30);
  padding: 0 vw-sp(50) 0 vw-sp(110);
  width: 100%;
  background-color: #e9f9f2;
  border-radius: .5em;
  height: vw-sp(110);
  font-size: vw-sp(28);
  font-weight: 700;
  cursor: pointer;
}

input[type="radio"]:checked + span {
  background-color: $color-main;
  color: $color-base;
}

input[type="radio"] {
  display: none;
}

input[type="radio"] + span::before {
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

input[type="radio"]:checked + span::after {
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

  label {
    margin-bottom: vw-pc(10);
  }

  span {
    margin-bottom: vw-pc(20);
    padding: 0 vw-pc(50) 0 vw-pc(75);
    height: vw-pc(80);
    border-radius: .5em;
    font-size: vw-pc(18);
  }

  input[type="radio"] + span::before {
    left: vw-pc(20);
    width: vw-pc(40);
    height: vw-pc(40);
  }

  input[type="radio"]:checked + span::after {
    left: vw-pc(20);
    width: vw-pc(20);
    height: vw-pc(20);
    border: vw-pc(10) solid $color-base;
  }
}

@media screen and (min-width: $breakpoint2) {

  label {
    margin-bottom: 10px;
  }

  span {
    margin-bottom: 20px;
    padding: 0 50px 0 75px;
    height: 80px;
    font-size: 18px; font-size: 1.8rem;
  }

  input[type="radio"] + span::before {
    left: 20px;
    width: 40px;
    height: 40px;
  }

  input[type="radio"]:checked + span::after {
    left: 20px;
    width: 20px;
    height: 20px;
    border: 10px solid $color-base;
  }
}


</style>
