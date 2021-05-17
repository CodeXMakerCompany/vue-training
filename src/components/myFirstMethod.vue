<template>
  <div class="">
    <b-button v-on:click="activateOnClick">{{ action }}</b-button>
    <p v-if="act != ''">{{ act }}</p>
    <p></p>
  </div>
</template>

<script>
export default {
  name: "MyFirstMethod",
  data() {
    return {
      act: ""
    };
  },
  props: {
    action: String
  },
  methods: {
    activateOnClick() {
      return this.act.length
        ? (this.act = "")
        : (this.act = "Oh god I was clicked");
    }
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
