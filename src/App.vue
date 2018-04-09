<template>
  <div id="app">
    <MediaQuery>
      hello
    </MediaQuery>
  </div>
</template>

<script>
import MediaQuery from './components/MediaQuery'
export default {
  name: 'app',
  components: {
    MediaQuery
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
