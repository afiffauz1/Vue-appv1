<template>
  <header>
    <h1 @click="changeTitle">{{ title }}</h1>
  </header>
</template>

<script>
import { bus } from "../main";

export default {
  props: {
    title: {
      type: String
    }
  },
  data() {
    return {
      title: "AFIF VUE APPv1"
    };
  },
  methods: {
    changeTitle: function() {
      //this.$emit("changeTitle", "Wow bisa gitu yah :v");
      this.title = "wow bisa berubah";
      bus.$emit("titleChanged", "wow bisa berubah");
    }
  }
};
</script>

<style scoped>
header {
  background: #240b36;
  padding: 10px;
}
h1 {
  color: #fff;
  text-align: center;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
