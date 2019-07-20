<template>
  <div>
    <button @click="increase"> + </button>
    <input v-model="countNumber">
    <button @click="decrease"> - </button>
  </div>
</template>

<script>
export default {
  name: 'IncreaseAndDecrease',
  data(){
    return{
      countNumber:0
    }
  },
  methods:{
    increase(){
      this.countNumber++;
      this.$emit("increase");
    },
    decrease(){
      this.countNumber--;
      this.$emit("decrease");
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