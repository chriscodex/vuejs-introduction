<template>
  <ul>
    <ChildComp v-for="(item, index) in lista" :key="index" :element="item" />
  </ul>
</template>

<script setup lang="ts">
import ChildComp from './ChildComp.vue';
const lista = ['uno', 'dos', 'tres', 'cuatro', undefined];
</script>

<style scoped></style>
