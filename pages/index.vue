<script lang="ts" setup>
const first = ref('test');
 function changeFirst (){

  first.value = 'autre chose';
 }


</script>


<template>
  <div>
    {{ first }}

  </div>
  <button @click='changeFirst()'>click</button>
</template>

<style scoped></style>
