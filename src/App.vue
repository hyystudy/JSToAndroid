<template>
  <div id="app">
    <img src="./assets/logo.png">
    <router-view/>
  </div>
</template>

<script>
  var helloComponent;
  export default {
    name: 'App',
    methods: {
      setComponent: function (component) {
        helloComponent = component
      },
      }
  }

  window['receiveMsg'] = function (msg) {
    helloComponent.changHello(msg)
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
</style>
