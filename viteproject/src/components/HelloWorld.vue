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
var myFunciton = function(x){data.count=data.count++}

</script>


<template>
  <p> ilosc towarow w koszyku: {{count}}</p>
  <p> Lista towarow: </p>
  <p v-for="d of data"> {{ d.name }} , {{ d.price }} <button @click=myFunciton(d.count)>Dodaj</button> </p>
  
<hr>
 
   <p v-for="d of data"> {{ d.name }}, {{d.count}} </p>

<hr>
  
</template>

<style scoped>
a {
  color: #42b983;
}
</style>
