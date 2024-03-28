<script setup>
import { ref } from 'vue'

defineProps ({
  height: String,
  weight: String,
  bmi: String

})


const emit = defineEmits([
  'stats-entered'

])
const height = ref('0')
const weight = ref('0')

const bmi = ref('weight / ( height * height')


function statsEntered(){
 // alert('do the math height' + height)
  emit('stats-entered', height.value,weight.value, bmi.value)
  
}
</script>

<template>

<label>Height in meters </label>
<input v-model ="height">

<p>
<label>Weight in kilograms</label>
<input v-model = "weight">
</p>


<button v-on:click ="statsEntered">Calculate</button>  
  
</template>

<style scoped>

button {
  background-color: aquamarine;
  margin: 10px;
}


</style>
