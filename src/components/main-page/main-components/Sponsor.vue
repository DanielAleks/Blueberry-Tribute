<template>
  <div class="sponsor-bg">
    <div class="sponsor-container">
      <div class="inner-bg" />
      <p>
        Sponsored by <b>blueberries</b>, get some yummies in your tummies at
        your local grocery store. Their not cheap, but they’re good.
      </p>
      <a href="">
        <img class="yokes" src="../../../assets/images/yokes.png" />
      </a>
      <a
        target="_blank"
        href="https://www.fredmeyer.com/p/blueberries/0003338322241"
      >
        <img class="fred-meyer" src="../../../assets/images/fred-meyer.png" />
      </a>
      <a
        href="https://www.walmart.com/grocery/ip/Fresh-Blueberries-24-oz/51259397"
      >
        <img class="walmart" src="../../../assets/images/walmart.png" />
      </a>
      <a href="https://www.traderjoes.com/digin/tag/Blueberries">
        <img class="trader-joes" src="../../../assets/images/trader-joes.png" />
      </a>
      <a href="https://www.safeway.com/shop/product-details.184070083.html">
        <img class="safeway" src="../../../assets/images/safeway.png" />
      </a>
      <a
        href=" https://www.target.com/p/blueberries-1-pint-package/-/A-13208898"
      >
        <img class="target" src="../../../assets/images/target.png" />
      </a>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass">
.yokes, .fred-meyer, .walmart, .trader-joes, .target, .safeway
  z-index: 100
  position: absolute
  height: 6rem
  width: 10rem
.yokes
  bottom: 15%
  left: 5%
.fred-meyer
  height: 4rem
  width: 13rem
  bottom: 15%
  left: 38%
.walmart
  width: 12rem
  height: 5rem
  bottom: 15%
  right: 5%
.trader-joes
  width: 12rem
  height: 4rem
  top: 17%
  right: 5%
.target
  width: 6rem
  height: 6rem
  top: 15%
  left: 45%
.safeway
  height: 4rem
  width: 15rem
  top: 17%
  left: 5%

.sponsor-bg
  height: 40vh
  width: 100%
  background: url('../../../assets/images/blueberriesSponsor.jpg')
  display: flex
  justify-content: center
.sponsor-container
  height: 100%
  width: 55rem
  position: relative
  display: flex
  justify-content: center
  align-items: center
  p
    width: 80%
    font-size: 2rem
    z-index: 1
  .inner-bg
    position: absolute
    background: #4382FF
    opacity: .95
    filter: blur(5px)
    height: 80%
    width: 100%
    border-radius: 10px
    z-index: 1
</style>
