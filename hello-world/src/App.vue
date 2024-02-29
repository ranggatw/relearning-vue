<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <div>HEllo {{ name }}</div>
  <div v-text="channel"></div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  data() {
    return {
      name: "rangga",
      channel: "r-code"
    }
  }
}
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
