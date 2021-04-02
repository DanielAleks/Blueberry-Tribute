<template>
  <div class="nav">
    <router-link to="/"> <p>Home</p> </router-link> |
    <router-link to="/recipes"> <p>Recipes</p></router-link> |
    <router-link to="/freezing"> <p>Freezing</p></router-link>
  </div>
  <router-view />
</template>

<script lang="ts"></script>

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

p
  font-size: 2rem

.nav
  padding: 30px
  color: black
  display: flex
  p
    margin: 10px
</style>
