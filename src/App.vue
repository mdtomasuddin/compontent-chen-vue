<script setup>
import { ref } from 'vue';
import TaskList from './components/TaskList.vue';

 
 const taskList=ref([
  {id:1, name:"task 1" , completed: false },
  {id:2, name:"task 2" , completed: false },
  {id:3, name:"task 3" , completed: false },
  {id:4, name:"task 4" , completed: false },
  {id:5, name:"task 5" , completed: false },
 ])
</script>
 
<template >
<p class="text-center text-4xl">Task Products</p>
<hr>
<p class="m-10">{{ taskList }}</p>
<div>
  <task-list :tasks="taskList" />
</div>
</template>
 
<style scoped>
 
</style>