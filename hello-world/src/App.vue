<template>
  <img alt="Vue logo" src="./assets/logo.png" />
  <h2 v-bind:id="headingId">This is Heading attribute</h2>
  <div>
    <div>
      <button v-bind:disabled="isDisabled">Bind</button>
    </div>
    <div>
      <button v-bind:disabled="!isDisabled">Bind</button>
    </div>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      headingId: "heading",
      isDisabled: true,
    };
  },
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
