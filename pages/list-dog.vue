<script lang="ts" setup>
import { Dog } from 'entities';

const {data} =  useFetch<Dog[]>('http://localhost:8000/api/dog');



</script>

<template>
  <DogItem v-for="item of data" :dog="item"/>
</template>

<style scoped></style>
