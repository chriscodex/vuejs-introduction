<template>
  <li>{{ element }}</li>
</template>

<script setup lang="ts">
defineProps({
  // element: String,
  element: {
    default: 'default',
  }
});
</script>

<style scoped></style>
