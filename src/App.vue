<template>
  <div>
    <app-header v-bind:title="title"></app-header>
    <app-members v-bind:members="members"></app-members>
    <app-footer v-bind:title="title"></app-footer>
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
    return {
      title: "AFIF VUE APPv1",
      members: [
        { name: "Muhammad", speciality: "Front-end", show: false },
        { name: "Afif", speciality: "UX Analitic", show: false },
        { name: "Fauzi", speciality: "UI Designer", show: false },
        { name: "Afif Fauzi", speciality: "Vue Expert", show: false },
        { name: "Muhammad Afif", speciality: "React Expert", show: false },
        {
          name: "Muhammad Afif Fauzi",
          speciality: "Front-end Engineer",
          show: false
        }
      ]
    };
  },
  methods: {
    updateTitle: function(updatedTitle) {
      this.title = updatedTitle;
    }
  }
};
</script>

<style>
</style>
