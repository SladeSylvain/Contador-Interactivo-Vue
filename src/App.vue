<template>
  <h1 v-bind:style="waffle">Bienvenido {{nombre}}</h1>
  <div v-bind:style="centrar">
  <button  @click="decremento">-</button>
  <span>{{contador}}</span>
  <button @click="incremento">+</button>

  <div v-if="contador<0">Negativo</div>
  <div v-else-if="contador>0">Positivo</div>
  <div v-else="contador">Valor 0</div>
  </div>
</template>

<script setup>
import {ref} from "vue"
const nombre = "Alexander"
const waffle = "color:gray;font-size:30px;text-align:center"
const centrar = "color:gray;font-size:20px;text-align:center"
const contador = ref(0)
const incremento= ()=>{
  contador.value++
}
const decremento = ()=>{
  contador.value--
}

</script>

<style scoped>
body{
  text-align: center;
}
</style>