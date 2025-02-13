<script setup>
 const props=defineProps(['countries']);
 import country from './country.vue';
</script>
 
<template>
<hr>
<p class=" text-2xl text-center">Country Components</p>
<ul class=" m-10 text-center">
    <country v-for="country in countries" :key="country.name" :country="country" />
</ul>
</template>
 
<style scoped>
 
</style>