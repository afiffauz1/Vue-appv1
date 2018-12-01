<template>
  <header>
    <h1>{{ title }}</h1>
  </header>
</template>

<script>
export default {
  data() {
    return {
      title: "AFIF VUE APPv1"
    };
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
