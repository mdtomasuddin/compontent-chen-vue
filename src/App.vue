<script setup>
import { ref } from 'vue';
import contriesComponent from './components/contriesComponent.vue';

 const saarcCountry=ref([
  {name: "Bangladesh", population: 169400000,  capital: "Dhaka"},
  {name: "India", population: 1417000000,  capital: "New Delhi"},
  {name: "USA", population: 331900000,  capital: "Washington"},
  {name: "Germany", population: 83200000,  capital: "Berlin"},
  {name: "Japan", population: 125800000,  capital: "Tokyo"}
])

function addCountry(){
  saarcCountry.value.push({name:"country-t", population:4123, capital:"tom"})
}
</script>
 
<template >
  <h1 class=" text-center text-5xl mb-10">List of Country</h1>
  <hr>
  <p class="m-10">{{ saarcCountry }}</p>

<contries-component  :countries="saarcCountry" />
<p class=" text-center">
  <button @click="addCountry()" class=" border-2 bg-gradient-to-b rounded">Add New Country</button>
</p>
</template>
 
<style scoped>
 
</style>