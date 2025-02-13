<script setup>
 import { ref } from 'vue';
import Task from './Task.vue';
 const props= defineProps(['tasks'])

 const add=ref(false)
 const newtask=ref({
    id:0,
    name:'',
    completed:false
 })

 function saveTask(){
 add.value=false
 newtask.value.id=props.tasks.length+1;
props.tasks.push(newtask.value)
 }
</script>
 
<template>
 <ul>
    <Task v-for="task in tasks"  :key="task.id" :task="task"/>
 </ul>

 <p>
    <button @click="add=true" class=" border-2">Add New Task</button>
 </p>
 <p v-show="add">
    new Task  : <input type="text" v-model="newtask.name">
    <button @click="saveTask()">Save</button>
 </p>
</template>
 
<style scoped>
 
</style>