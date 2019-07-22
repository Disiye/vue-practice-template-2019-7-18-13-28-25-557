<template>
  <div id="app">
    <button @click="increase"> + </button>
    <input id="input" v-model="this.$store.state.count">
    <button @click="decrease"> - </button>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
    }
  },
  methods:{
    increase(){
      this.$store.commit("increment")
    },
    decrease(){
      this.$store.commit("decrement")
    }
    
  }
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
