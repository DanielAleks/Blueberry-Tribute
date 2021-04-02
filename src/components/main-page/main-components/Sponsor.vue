<template>
  <div class="sponsor-bg">
    <div class="sponsor-container">
      <div class="inner-bg" />
      <p>
        Sponsored by blueberries, get some yummies in your tummies at your local
        grocery store. Their not cheap, but they’re good.
      </p>
    </div>
  </div>
</template>

<script></script>

<style lang="sass">
.sponsor-bg
  height: 40vh
  width: 100%
  background: url('../../../assets/images/blueberriesSponsor.jpg')
  display: flex
  justify-content: center
  .sponsor-container
    height: 100%
    width: 30%
    position: relative
    display: flex
    justify-content: center
    align-items: center

    p
      width: 80%

      font-size: 2.5rem
      z-index: 1
  .inner-bg
    position: absolute
    background: #fffbe7
    opacity: .9
    height: 80%
    width: 100%
    border-radius: 10px
    z-index: 0
</style>
