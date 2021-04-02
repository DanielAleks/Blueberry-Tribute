<template>
  <div class="home-container">
    <div class="blueberries-bg" />
    <div class="tribute-title-container">
      <p>A Tribute to</p>
      <p class="tribute-blueberry">Blueberries</p>
    </div>
  </div>
</template>

<script lang="ts"></script>

<style lang="sass">
.home-container
  height: 90vh
  width: 100%
  position: relative
.blueberries-bg
  background: url('../../../assets/images/blueBest.png')
  height: 85vh
  width: 68%
  position: absolute
  z-index: 0
  right: 10vw
  transform: rotate(180deg)
  background-size: cover
  background-position: 50% 50%
.tribute-title-container
  position: absolute
  width: 50rem
  top: 25%
  p
    font-size: 12rem
    font-family: Rubik
    font-weight: 900
    margin: 0px
.tribute-blueberry
  background-image: url('../../../assets/images/blueberriesSponsor.jpg')
  color: transparent
  -webkit-background-clip: text
  font-size: 28vw
  position: absolute
  background-size: cover
  font-weight: 900
  text-align: center
  // background: url('../../../assets/images/blueberriesSponsor.jpg')
  // -webkit-background-size: cover
  // -moz-background-size: cover
  // -o-background-size: cover
  // background-size: cover
  // color: red
</style>
