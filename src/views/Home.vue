<template>
  <div class="home">
    <MainPage msg="Welcome to Your Vue.js + TypeScript App" />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import MainPage from "@/components/main-page/MainPage.vue"; // @ is an alias to /src

@Options({
  components: {
    MainPage,
  },
})
export default class Home extends Vue {}
</script>
