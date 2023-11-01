<template>
  <ul>
    <ChildComp
      v-for="(item, index) in lista"
      :key="index"
      :element="item"
      @removeElement="removeElement(index)"
    />
  </ul>
</template>

<script setup lang="ts">
import ChildComp from './ChildComp.vue';
import { ref } from 'vue';
const lista = ref(['uno 1', 'dos 2', 'tres 3', 'cuatro 4', undefined]);

const removeElement = (indexRemove) => {
  const newLista = lista.value.filter((listElement, listIndex) => {
    return listIndex !== indexRemove;
  });
  lista.value = [...newLista];
};
</script>

<style scoped></style>
