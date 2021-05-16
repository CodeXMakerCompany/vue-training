<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png" />
    <Main msg="Well well well, see who's here." />
    <p class="container">
      <b-alert variant="success" show
        >From main component : {{ courseGoal }}</b-alert
      >
    </p>
    <p class="container">
      <b-alert variant="success" show>
        <a v-bind:href="link">Codexmaker Page</a></b-alert
      >
    </p>
  </div>
</template>

<script>
import Main from "./components/main.vue";

export default {
  name: "App",
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Main
  },
  data() {
    return {
      courseGoal: "Learn vue", //String
      link: "https://codexmaker.xyz/"
    };
  }
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
