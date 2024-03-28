<script setup>
import BodyMassIndexForm from './components/BodyMassIndexForm.vue'

import { ref } from 'vue'
const bmi = ref('')
const bmiHeight = ref('')
const bmiWeight = ref('')

 
 const calculateBMI = (heigth,weight,bim)=>{
  bmi.value = heigth,weight,bim
 }
</script>

<template>

 <div id="app-component"> 

    <h1>Body Mass Index Calculator</h1>
    
  

    <BodyMassIndexForm
    v-bind:bmi = "bmiHeight"
    v-bind:heigth = "bmiHeight"
    v-bind:weight="bmiWeight"
    v-on:stats-entered="calculateBMI"/>

 
   <p> {{ bmi }} </p>
</div>

 

</template>

<style scoped>



</style>
