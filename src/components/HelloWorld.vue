<template>
  <div class="hello">
    <h1>{{ msg }}</h1>
    <div>{{hello}}</div>
    <button @click="callAndroid">调用Android方法</button>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  data () {
    return {
      msg: 'Welcome to Your Vue.js App',
      hello: 'Hello World',
    }
  },
  methods: {
    changHello: function (msg) {
      this.hello = msg
    },
    callAndroid: function (){
      //调用Android的方法 提前需要和Android端对接一下
      window.android.showInfoFromJs('你好我来自web端')
    }
  },
  created() {
    this.$parent.setComponent(this)
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1, h2 {
  font-weight: normal;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
