<template>
  <li @click="$emit('removeElement')">{{ element }}</li>
</template>

<script setup lang="ts">
defineProps({
  element: {
    default: 'default',
  },
});
</script>

<style scoped></style>
