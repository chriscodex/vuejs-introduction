<script setup lang="ts">
import { ref, computed, watch } from 'vue';
  const texto = ref('Initial Text')
  const open = ref(false);
  const firstName = 'Christian'
  const lastName = 'Espinoza'

  const puertaLabel = ref('Puerta Cerrada')

  const fullName = computed(() => {
    return `${firstName} ${lastName}`
  })

  // Vigilar cambios en el texto
  watch(texto, (newText, oldText) => {
    console.log('texto cambiado', newText, oldText)
  }, )

  watch(open, (newValue) => {
    if (newValue) {
      puertaLabel.value = 'Puerta Abierta'
    } else {
      puertaLabel.value = 'Puerta Cerrada'
    }
  })

  const computedLabel = computed(() => {
    return open.value ? 'Cerrar' : 'Abrir'
  })
</script>

<template>
  <p>{{texto}}</p>
  <!-- <input type="text" :value="texto" @input="inputChange"/> -->
  <input type="text" v-model="texto"/>
  <p>Full Name {{fullName}}</p>
  <p>Ejercicio</p>
  <p>{{puertaLabel}}</p>
  <button @click="open = !open">{{computedLabel}}</button>
</template>

<style scoped>
  input {
    border: 1px solid #ccc;
    margin-right: 10px;
  }
</style>