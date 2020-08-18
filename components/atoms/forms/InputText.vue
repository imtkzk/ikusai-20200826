<template>
    <dl class="pay-input">
        <dt><slot /></dt>
        <dd><input :type="type" :placeholder="placeholder"></dd>
     </dl>
</template>

<script>
export default {
    props:[
        `placeholder`,
        `type`
    ]
}
</script>

<style lang="scss" scoped>
    @import "~assets/scss/style.scss";


.pay-input {
  margin-bottom: vw-sp(50);
}

.pay-input dt {
  display: block;
  width: 100%;
  margin-bottom: .7em;
  font-weight: 700;
}

.pay-input dd {
  display: block;
  width: 100%;
}

.pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
  padding: 1em 1em;
  background-color: #f8f8f8;
  border: 1px solid $color-main;
  border-radius: .5em;
  width: 100%;
  max-width: 100%;
  color: $color-text;
  font-family: $font1;
  font-size: vw-sp(25);
  font-weight: 700;
  letter-spacing: .1em;
}

@media screen and (min-width: $breakpoint1) {

  .pay-input {
    margin-bottom: vw-pc(40);
    width: vw-pc(485);
  }

  .pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
    font-size: vw-pc(15);
  }
}

@media screen and (min-width: $breakpoint2) {

  .pay-input {
    margin-bottom: 40px;
    width: 485px;
  }

  .pay-input input[type="text"], .pay-input input[type="email"], .pay-input input[type="tel"] {
    font-size: 15px;
  }
}


</style>
