<template>
  <div>
    <div v-for="value in inputNumber" :key=value>
        <IncreaseAndDecrease></IncreaseAndDecrease>
    </div>
  </div>
</template>

<script>
import IncreaseAndDecrease from './IncreaseAndDecrease'
export default {
  name: 'CounterGroup',
  components:{IncreaseAndDecrease},
  props: ['inputNumber'],
  data(){
    return{
        
    }
  }
}
</script>