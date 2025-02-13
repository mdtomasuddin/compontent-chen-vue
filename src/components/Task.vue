<script setup>
 defineProps(['task'])
</script>
 
<template>
<li class="ml-10 mb-2">
   Id: {{ task.id }} <input  type="checkbox" v-model="task.completed" /> -{{ task.name }}
</li>
</template>
 
<style scoped>
 
</style>