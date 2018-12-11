<template>
  <div id="members">
    <ul>
      <li v-for="member in members" @click="member.show = !member.show">
        <h2>{{member.name}}</h2>
        <h3 v-show="member.show">{{member.speciality}}</h3>
      </li>
    </ul>
    <button @click="deleteMember">Delete Member</button>
  </div>
</template>

<script>
export default {
  props: {
    members: {
      type: Array,
      required: true
    }
  },
  data() {
    return {};
  },
  methods: {
    deleteMember: function() {
      this.members.pop();
    }
  }
};
</script>

<style scoped>
#members {
  width: 100%;
  max-width: 1200%;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 30px;
  border: 1px solid black;
  margin: 10px;
}
</style>
