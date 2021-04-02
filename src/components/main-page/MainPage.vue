<template>
  <div class="main-container">
    <Home />
    <Sponsor />
    <Benefits />
  </div>
</template>

<script lang="ts">
import { Options, Vue } from "vue-class-component";
import Sponsor from "./main-components/Sponsor.vue";
import Benefits from "./main-components/Benefits1.vue";
import Home from "./main-components/Home.vue";

@Options({
  components: {
    Home,
    Sponsor,
    Benefits,
  },
  props: {
    msg: String,
  },
})
export default class HelloWorld extends Vue {
  msg!: string;
}
</script>

<style lang="sass">
.main-container
  height: 100vh
</style>
