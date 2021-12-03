<template>
  <div class="">
    <landing-page />
  </div>
</template>

<script>
import LandingPage from './views/LandingPage.vue'

export default {
  name: 'App',
  components: {
    LandingPage
  }
}
</script>

<style>

* {
   margin: 0;
   padding: 0;
}
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  background-image:
    linear-gradient(
      #019FF9, #054D75
    );
  height: 100vh;
  overflow: hidden;
}
</style>
