<template>
  <div>
    <app-header></app-header>
    <app-members></app-members>
    <app-footer></app-footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Footer from "./components/Footer.vue";
import Member from "./components/Members.vue";

export default {
  components: {
    "app-header": Header,
    "app-footer": Footer,
    "app-members": Member
  },
  data() {
    return {};
  }
};
</script>

<style>
</style>
