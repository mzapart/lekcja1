<script setup>
import { ref } from 'vue'
import data from '../data.js'

defineProps({
  msg: String
})

const count = ref(0)
var products = {
  apple: 2.5,
  pear: 4,
  grape: 0.1
};
</script>

<template>
  <p> ilosc towarow w koszyku: {{count}}</p>
  <p> lista towarow: </p>
<hr>

   <p v-for="d of data">Nazwa: {{ d.name }}, Cena: {{ d.price }}, <button onclick="myFunction(){d.count++, count++}">Click me</button>, {{d.count=0}} </p>

<hr>
  
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
