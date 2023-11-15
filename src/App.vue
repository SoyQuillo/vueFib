<script setup>

import { ref } from 'vue'

let numberEnter = ref(0);
let aux = ref(0);
let fib = [0,1];

function fibonacci (numberEnter) {

for(let i = 2; i <= numberEnter; i++){

fib[i] = fib[i-1] + fib[i-2];

}

return fib[numberEnter];

}

function doClick(){

aux.value = numberEnter.value;

}


</script>

<template>

 <input v-model="numberEnter" type="number">
  <button @click="doClick">PRESIONAR</button>
  <h1>{{ fibonacci(aux) }}</h1>
</template>

<style scoped>

</style>
