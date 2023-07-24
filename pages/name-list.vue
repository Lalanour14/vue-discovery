<script lang="ts" setup>
const names = ref(['fifi','riri','loulou','lili']);
const newName = ref('');
function addName(){
  names.value.push(newName.value) ;
}

</script>
<template>
  <div>
    <input type="text" v-model="newName" placeholder="type a name ...">
    <button @click="addName()"> Add</button>
  <ul>
    <li v-for=" item of names">{{item}}</li>
    
  </ul>
  </div>
</template>

<style scoped></style>
