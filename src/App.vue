<template>
  <div id="app">
    <Head></Head>
    <router-view/>
  </div>
</template>

<script>
import Head from './components/menu'

export default {
  name: 'App',
  components: {
    Head
  }
}
</script>

<style>
body {
  margin: 0;
  padding: 0;
}

h1, h2, h3, p {
  margin: 0;
  padding: 0;
}

#app {
  /* font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px; */
}
</style>
