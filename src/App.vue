<template>
  <div id="app">
    <!--<img src="./assets/logo.png">-->
    <div class="contentdiv">
      <router-view/>
    </div>
  </div>
</template>

<script>
export default {
  name: 'App'
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.contentdiv {
  background:url("./assets/image/login.jpg") no-repeat center fixed;
  background-size:contain;
  background-size: cover;
  -webkit-background-size: cover;
  height: 90%;
}
</style>
