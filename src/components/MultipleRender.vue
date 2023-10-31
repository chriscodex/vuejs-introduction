<template>
  <div class="container">
    <div class="list">
      <div v-for="(item, index) in posts" :key="index" class="item">
        <div>{{ item.title }}</div>
        <p>{{ item.description }}</p>
      </div>
    </div>
  </div>
</template>

<script setup lang="ts">
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
.item {
  border: 1px solid white;
  padding: 1px;
}
</style>
