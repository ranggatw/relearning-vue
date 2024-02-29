<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h2 class="underline">This is text underline</h2>
  <h2 v-bind:class="status">This is Binding Classes</h2>
  <h2 class="underline" v-bind:class="status">This is Binding Classes and add class style</h2>
  <hr />
  <div v-bind:class="isPromoted && 'promoted'">This is Promoted</div>
  <div v-bind:class="isSoldOut ? 'sold-out' : 'new' ">Sold out ? Movie</div>
  <hr />
  <div v-bind:class="['new', 'promoted']">Newly Promoted movie</div>
  <div v-bind:class="[isPromoted && 'promoted', isSoldOut ? 'sold-out': 'new']">Array Conditional movie</div>
  <div v-bind:class="{
    promoted: isPromoted,  
    new: !isPromoted,
    'sold-out': isSoldOut
  }">Object Conditional movie</div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      status: 'danger',
      isPromoted:  false,
      isSoldOut: true
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

.underline {
  text-decoration: underline;
}

.promoted {
  color: green;
  font-style: italic;
}

.new {
  color: olivedrab;
}

.sold-out {
   color: red;
}

</style>
