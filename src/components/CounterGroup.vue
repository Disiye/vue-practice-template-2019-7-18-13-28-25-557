<template>
  <div>
    <div v-for="value in inputNumber" :key=value>
        <IncreaseAndDecrease @increase="sumIncrease" @decrease="sumDecrease"></IncreaseAndDecrease>
    </div>
    <div>
      <couter-sum :counterSum="sum"></couter-sum>
    </div>
  </div>
</template>

<script>
import IncreaseAndDecrease from './IncreaseAndDecrease'
import CouterSum from "./CounterSum"
export default {
  name: 'CounterGroup',
  components:{
    IncreaseAndDecrease,
    CouterSum
    },
  props: ['inputNumber'],
  methods: {
      sumIncrease(){
          this.sum++;
      },
      sumDecrease(){
          this.sum--;
      }
  },
  data(){
    return{
        sum:0
    }
  }
}
</script>