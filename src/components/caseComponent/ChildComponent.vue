<template>
  <div class="item">
    <div>{{ props.post.title }}</div>
    <p>{{ props.post.description }}</p>
  </div>
</template>

<script setup lang="ts">
const props = defineProps(['post']);
</script>

<style scoped>
.item {
  border: 1px solid white;
  padding: 1px;
}
</style>
