<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <HelloWorld msg="Welcome to Vue.js App - Tam-NLT"/>

    <div>
      <p>Two way binding in Vue</p>
    <div v-show="isShow">
      <p>Two way binding in Vue</p>
    </div>
    <button @click="isShow = !isShow">Hidden</button>
    <button @click="count++">Count</button>
    {{ count }}
    </div>

</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  data () {
    return {
      isShow: true,
      count: 0
    }
  },
  updated () {
    return {
      count: 2
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
