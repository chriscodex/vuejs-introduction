<script setup lang="ts">
import { ref, computed } from 'vue';
  const texto = ref('Initial Text')
  const firstName = 'Christian'
  const lastName = 'Espinoza'
  const fullName = computed(() => {
    return `${firstName} ${lastName}`
  })

  const inputChange = (e: any) => {
    texto.value = e.target.value
  }

  const computedText = computed(() => {
    return texto.value.toUpperCase()
  })
</script>

<template>
  <p>{{texto}}</p>
  <input type="text" :value="texto" @input="inputChange"/>
  <input type="text" v-model="texto"/>
  <p>{{computedText}}</p>
  <p>Full Name {{fullName}}</p>

</template>

<style scoped>
  input {
    border: 1px solid #ccc;
    margin-right: 10px;
  }
</style>