<script lang="ts" setup>

import { Dog} from "../entities";

defineProps<{
  dog:Dog
}> ()

</script>

<template>
  <div>
    <h3><NuxtLink :to="'/dog'+dog._id"></NuxtLink> {{ dog.name }}</h3>
    <p>{{ dog.breed }}</p>
    <p>{{ dog.birthdate }}</p>
  </div>
</template>

<style scoped></style>
