<template>
  <div v-html="html"></div>
</template>

<script>
export default {
  name: "BindHtml",
  props: {
    html: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped></style>
