<script lang="ts" setup>
import { Dog } from '../entities';

const emit = defineEmits(['submitDog']);

const dog = ref<Dog>({name:"",breed:"",birthdate:""});

 function handleSubmit(){
  console.log(dog);
  emit('submitDog',dog.value);

 }


</script>

<template>
  <div>
  <form @submit.prevent="handleSubmit()">
    <label for="name">Name</label>
   <input type="text" v-model="dog.name"  id="name">
   <label for="breed">Breed</label>
   <input type="text" v-model="dog.breed" id="breed">
   <label for="name">birthdate</label>
   <input type="text" v-model="dog.birthdate"  id="birthdate">
    <button >Submit</button>
  </form>
  </div>
</template>

<style scoped></style>
