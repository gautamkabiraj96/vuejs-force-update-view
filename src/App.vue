<template>
  <div id="app">
    <button @click="addProperties">Add new properties</button>
    <div v-for="(value, i) in person" :key="i">
      {{ value }}
    </div>
    <div class="np-credits">wwww.nightprogrammer.com</div>
  </div>
</template>

<script>
import Vue from "vue";

export default {
  name: "App",
  data() {
    return {
      person: {
        name: "Gautam",
      },
    };
  },
  methods: {
    addProperties() {
      //this.foo.b = 2;
      //Vue.set(this.person, "age", 27);
      //this.$set(this.person, "age", 27);
      // this.person = Object.assign({}, this.person, {
      //   age: 27,
      //   nationality: "Indian",
      // });
      this.person = { ...this.person, nationality: "Indian" };
    },
  },
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  padding: 24px;
}

button {
  background-color: #004cbe;
  color: #ffffff;
  border: 0px;
  border-radius: 6px;
  padding: 6px 20px;
  margin-right: 1em;
  cursor: pointer;
  transition: all 0.3s;
  margin-bottom: 8px;
}

button:hover {
  background-color: #2f79e7;
  transition: all 0.3s;
}

.np-credits {
  font-size: 12px;
  margin-top: 12px;
  color: #4b4b4b;
}
</style>