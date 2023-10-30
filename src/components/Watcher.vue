<script setup lang="ts">
import { ref, computed, watch } from 'vue';
  const texto = ref('Initial Text')
  const firstName = 'Christian'
  const lastName = 'Espinoza'
  const fullName = computed(() => {
    return `${firstName} ${lastName}`
  })

  // Vigilar cambios en el texto
  watch(texto, () => {
    console.log('texto cambiado')
  })
</script>

<template>
  <p>{{texto}}</p>
  <!-- <input type="text" :value="texto" @input="inputChange"/> -->
  <input type="text" v-model="texto"/>
  <p>Full Name {{fullName}}</p>
</template>

<style scoped>
  input {
    border: 1px solid #ccc;
    margin-right: 10px;
  }
</style>