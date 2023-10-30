<script setup lang="ts">
import { ref } from 'vue';
  const texto = ref('Initial Text')

  const inputChange = (e: any) => {
    texto.value = e.target.value
  }
</script>

<template>
  <div>
    <p>{{texto}}</p>
    <input type="text" :value="texto" @input="inputChange"/>
    <input type="text" v-model="texto"/>
  </div>

</template>

<style scoped>
  input {
    border: 1px solid #ccc;
    margin-right: 10px;
  }
</style>