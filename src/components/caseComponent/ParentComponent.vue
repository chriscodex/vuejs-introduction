<template>
  <div class="container">
    <div class="list">
      <ChildComponent v-for="(item, index) in posts" :key="index" :post="item" />
    </div>
  </div>
</template>

<script setup lang="ts">
import ChildComponent from './ChildComponent.vue';

const posts = [
  {
    title: 'Titulo 1',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
  },
  {
    title: 'Titulo 2',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
  },
  {
    title: 'Titulo 3',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
  },
  {
    title: 'Titulo 4',
    description: 'Lorem ipsum dolor sit amet consectetur adipisicing elit.',
  },
];
</script>

<style scoped>
.list {
  display: flex;
  flex-direction: column;
}

</style>