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
    <p class="container">
      <b-alert variant="success" show>
        <!-- Binding an array -->
        <MyFirstMethod :action="actions[0]" />
      </b-alert>
    </p>
    <p class="container">
      <b-alert variant="success" show>
        <BindHtml :html="html" />
      </b-alert>
    </p>
  </div>
</template>

<script>
import Main from "./components/main.vue";
import MyFirstMethod from "./components/myFirstMethod";
import BindHtml from "./components/bindHtml";

export default {
  name: "App",
  components: {
    // eslint-disable-next-line vue/no-unused-components
    Main,
    MyFirstMethod,
    BindHtml
  },
  data() {
    return {
      courseGoal: "Learn vue", //String
      link: "https://codexmaker.xyz/",
      actions: ["My First Method", "dos", "tres"],
      html: "<h2>Embed html</h2>"
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
