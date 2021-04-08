<template>
  <div style="position: relative; height: 0px">
    <i @click="navModal = !navModal" class="fas fa-bars fa-4x sandwich-nav"></i>
    <div v-if="navModal" class="mobile-nav">
  <router-link class="nav-item" to="/"> Home</router-link> |
    <router-link class="nav-item" to="/recipes"> Recipes</router-link> |
    <router-link class="nav-item" to="/freezing"> Freezing</router-link>
      >
    </div>
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
// overflow: visible
@font-face
  font-family: "Nunito-Bold"
  src: url('./assets/fonts/Nunito-Bold.ttf')
@font-face
  font-family: "Nunito-Regular"
  src: url('./assets/fonts/Nunito-Regular.ttf')
@font-face
  font-family: "Rubik"
  src: url('./assets/fonts/static/Rubik-Black.ttf')

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
  width: 100%
  height: 15rem
  background: linear-gradient(180deg, rgba(67,130,255,1) 0%, rgba(91,146,255,1) 50%, rgba(67,130,255,1) 100%)
  box-shadow: 2px 3px 6px 0px #404040
  position: absolute
  top: 7rem
  z-index: 100111
  display: flex
  flex-direction: column
  align-items: center

.mobile-nav-item
  font-size: 2rem
  text-decoration: none
  color: black
  font-family: nunito-regular
  width: 100%
  height: 33%
  border: 1px solid #404040
  border-top: none
  margin: 0px
  cursor: pointer
  display: flex
  align-items: center
  justify-content: center
  z-index: 10000

.sandwich-nav
  // position: absolute
  display: none
  z-index: 100
  @media (max-width: 900px)
    position: absolute
    display: flex
    overflow:
    top: 3rem
    right: 4rem
    z-index: 10000

@keyframes slide-down-nav
  0%
    transform: translateY(-20rem)
  100%
    transform: translateY(0rem)

.nav
  animation: slide-down-nav 1s
  position: absolute
  color: black
  padding: 10px
  display: flex
  height: 0px
  right: 0px
  z-index: 100
  @media (max-width: 900px)
    display: none
.nav-item
  text-decoration: none
  font-size: 2.5rem
  color: black
  margin: 1rem
  margin-right: 5rem
  font-family: Nunito-regular
  font-weight: bold
</style>
