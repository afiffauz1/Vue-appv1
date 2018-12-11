<template>
  <footer>
    <p>{{ copyright }} {{title}}</p>
  </footer>
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
      copyright: "2018 - Muhammad Afif Fauzi - "
    };
  },
  created() {
    bus.$on("titleChanged", data => {
      this.title = data;
    });
  }
};
</script>

<style scoped>
footer {
  width: 100%;
  background-color: #c31432;
  color: white;
  text-align: center;
}
p {
  color: white;
  text-align: center;
  font-family: Arial, Helvetica, sans-serif;
}
</style>
