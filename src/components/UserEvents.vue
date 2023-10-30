<script setup lang="ts">
const submitEvent = (
  // e: Event
  ) => {
  // e.preventDefault()
  console.log('Enviado');
}
</script>

<template>
  <form @:submit.prevent="submitEvent">
  <!-- <form v-on:submit="submitEvent"> -->
    <h1>User Events</h1>
    <p>Formulario</p>
    <button>Submit</button>
  </form>
</template>

