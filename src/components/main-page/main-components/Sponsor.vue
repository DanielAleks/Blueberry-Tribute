<template>
  <div class="sponsor-bg">
    <div class="sponsor-container">
      <div class="inner-bg" />
      <p>
        Sponsored by <b>blueberries</b>, get some yummies in your tummies at
        your local grocery store. Their not cheap, but they’re good.
      </p>
    </div>
  </div>
</template>

<script>
export default {};
</script>

<style lang="sass">
.sponsor-bg
  height: 40vh
  width: 100%
  background: url('../../../assets/images/blueberriesSponsor.jpg')
  display: flex
  justify-content: center
  background-attachment: fixed
  background-position: center
  background-repeat: no-repeat
  background-size: cover
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
    height: 80%
    width: 100%
    border-radius: 10px
    z-index: 1
</style>
