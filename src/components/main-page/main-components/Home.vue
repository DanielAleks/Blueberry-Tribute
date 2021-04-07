<template>
  <div class="home-container">
    <div class="blueberries-bg" />
    <div class="tribute-title-container">
      <p class="tribute-text">A Tribute to</p>
      <p class="tribute-blueberry">Blueberries</p>
    </div>
    <i class="fas fa-chevron-down fa-4x down-styles"></i>
  </div>
</template>

<script lang="ts"></script>

<style lang="sass">
.down-styles
  position: absolute
  bottom: 1rem
  left: 50%
  animation: arrow-jump 2s infinite forwards
  opacity: 0
  display: flex
  flex-direction: column
  color: #313131

@keyframes arrow-jump
  0%
    opacity: 0
    transform: translateY(-10px)
  100%
    opacity: 1
    transform: translateY(0px)

.home-container
  height: 100vh
  width: 100%
  position: relative
.blueberries-bg
  background: url('../../../assets/images/png.png')
  height: 90rem
  width: 100rem
  position: absolute
  z-index: 0
  right: 0px
  background-size: cover
  background-position: 50% 50%
  @media (max-width: 1650px)
    right: -100px
  @media (max-width: 1550px)
    height: 80rem
    width: 90rem
  @media (max-width: 1400px)
    transform: rotate(-90deg)
    height: 85rem
    width: 85rem
    left: 0px
    top: 200px
.tribute-title-container
  position: absolute
  width: 60rem
  top: 25%
  left: 5%
  p
    font-family: Rubik
    margin: 0px
.tribute-text
  font-size: 12rem

.tribute-blueberry
  background-image: url('../../../assets/images/blueberriesSponsor.jpg')
  color: transparent
  -webkit-background-clip: text
  background-size: cover
  width: 130%
  font-size: 12rem

@media (max-width: 1400px)
  .tribute-title-container
    top: 25%
    right: 100px
    left: auto
  .tribute-text, .tribute-blueberry
    font-size: 9rem
@media (max-width: 1200px)
  .tribute-title-container
    right: 0px
  .blueberries-bg
    top: auto
    bottom: 0px
    height: 70rem
    width: 70rem

@media (max-width: 900px)
  .blueberries-bg
    transform: rotate(-90deg)
    height: 55rem
    width: 55rem
    left: 0px
  .tribute-title-container
    right: 5%
    top: 20%
  .tribute-text, .tribute-blueberry
    font-size: 8rem
@media (max-width: 750px)
  .blueberries-bg
  .tribute-title-container
    right: auto
    left: 100px
  .tribute-text, .tribute-blueberry
    font-size: 7rem
@media (max-width: 650px)
  .tribute-text, .tribute-blueberry
  .tribute-title-container
    left: 50px
@media (max-width: 550px)
  .tribute-title-container
    left: auto
    right: -30vw
  .tribute-text, .tribute-blueberry
    font-size: 6.5rem
  .blueberries-bg
    width: 50rem
    height: 50rem
</style>
