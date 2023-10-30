<template>
  <div>
    <h2>{{ labelTitle }}</h2>
    <div v-if="logged">
      <p>Hola, {{ username }}</p>
    </div>
    <div v-else>
      <p>Ingresa tu usuario</p>
      <input type="text" v-model="username" />
    </div>
    <button @click="logged = !logged">
      <p v-if="!logged">Acceder</p>
      <p v-else>Salir</p>
    </button>
  </div>
</template>

<script setup lang="ts">
import { ref, watch } from 'vue';
const labelTitle = ref('Iniciar Sesión');
const logged = ref(false);
const username = ref('');

watch(logged, () => {
  if (logged.value) {
    labelTitle.value = 'Cierre Sesión';
  } else {
    labelTitle.value = 'Iniciar Sesión';
    username.value = '';
  }
});
</script>

<style lang="scss" scoped></style>
