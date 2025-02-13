<script setup>
 defineProps(['country'])
</script>
 
<template>
    <li >
        <input  class="mb-1 border-2 backdrop-blur-100 border-solid" type="text" v-model="country.name" />
        -<input  class="mb-1 border-2 backdrop-blur-100 border-solid" type="text" v-model="country.capital" />
        -<input  class="mb-1 border-2 backdrop-blur-100 border-solid" type="text" v-model="country.population" /> 
    </li>
</template>
 
<style scoped>
 
</style>