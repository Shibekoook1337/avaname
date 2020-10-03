<template>
  <main-page />
</template>

<script>
import MainPage from './components/MainPage.vue';

export default {
  name: 'App',
  components: {
    MainPage
  }
}
</script>

<style>
* {
  box-sizing: border-box;
  font-family: Avenir, Helvetica, Arial, sans-serif;
}

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  /* color: #2c3e50; */
}
</style>
