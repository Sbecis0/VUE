<!--
https://eugenkiss.github.io/7guis/tasks/#temp
-->

<script setup>
import { ref } from 'vue'
  // importamos el vue
  
// agregamos dos variables con su valor corespondiente en 		neutro
const c = ref(0)
const f = ref(32)

// creamos una funcion que estlablece c 
function setC(e, v = +e.target.value) {
  c.value = v
  f.value = v * (9 / 5) + 32
}

// funcion que asigna los f
function setF(e, v = +e.target.value) {
  f.value = v
  c.value = (v - 32) * (5 / 9)
}
</script>

<template>
  
  <input type="number" :value="c" @change="setC"> Celsius =
  <input type="number" :value="f" @change="setF"> Fahrenheit

</template>
