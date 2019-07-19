<template>
  <div>
    <input id="input" v-model.number="inputNumber">
    <CounterGroup :inputNumber="inputNumber"></CounterGroup>
  </div>
</template>

<script>
import CounterGroup from './components/CounterGroup'
export default {
  name: 'app',
  components:{CounterGroup},
  data(){
    return {
      inputNumber: 0
    }
  }
}
</script>
