<template>
  <!-- <p v-if= >Hello</p> -->
  <i @click="navModal = !navModal" class="fas fa-bars fa-4x sandwich-nav"></i>
  <div v-if="navModal" class="mobile-nav">
    <router-link class="mobile-nav-item" to="/"> Home</router-link> |
    <router-link class="mobile-nav-item" to="/recipes"> Recipes</router-link> |
    <router-link class="mobile-nav-item" to="/freezing"> Freezing</router-link>
  </div>

  <div class="nav">
    <router-link class="nav-item" to="/"> Home</router-link> |
    <router-link class="nav-item" to="/recipes"> Recipes</router-link> |
    <router-link class="nav-item" to="/freezing"> Freezing</router-link>
  </div>
  <router-view />
</template>

<script>
export default {
  name: "app",
  data() {
    return {
      navModal: false,
    };
  },
};
</script>

<style lang="sass">
@font-face
  font-family: "Nunito-Bold"
  src: url('./assets/fonts/Nunito-Bold.ttf')
@font-face
  font-family: "Nunito-Light"
  src: url('./assets/fonts/Nunito-Light.ttf')
@font-face
  font-family: "Nunito-Regular"
  src: url('./assets/fonts/Nunito-Regular.ttf')
@font-face
  font-family: "Rubik"
  src: url('./assets/fonts/Rubik-VariableFont_wght.ttf')
@font-face
  font-family: "Rubik-Italic"
  src: url('./assets/fonts/Rubik-Italic-VariableFont_wght.ttf')

body, html
  margin: 0px !important
  padding: 0px !important
  background: #fffbe7
  font-size: 62.5%
  overflow-x: hidden

p
  font-size: 2rem
  text-decoration: none
  font-family: Nunito-regular

.mobile-nav
  width: 100vw
  height: 15rem
  background: red
  position: absolute
  top: 7rem

.sandwich-nav
  position: absolute
  display: none
  z-index: 1
  
  @media (max-width: 600px)
    display: flex
    top: 3rem
    right: 4rem

.nav
  padding: 30px
  color: black
  display: flex
  position: absolute
  right: 0px
  z-index: 100
  @media (max-width: 600px)
    display: none
.nav-item
  text-decoration: none
  font-size: 3rem
  color: black
  margin: 1rem
  margin-right: 5rem
  font-family: Nunito-regular
  font-weight: bold
</style>
