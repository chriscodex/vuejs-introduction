
<script setup lang="ts">
  import { computed, ref, watch } from 'vue';
  const puertaLabel = ref('Puerta cerrada')
  const open = ref(false)
  const puertaCondition = computed(() => {
    return open ? 'Abrir' : 'Cerrar'
  })
  const doorStyles = ref({
    backgroundColor: '#ee5',
    color: 'black',
    padding: '1px'
  })
  watch(open, (newValue) => {
    if (newValue) {
      puertaLabel.value = 'Puerta abierta'
      doorStyles.value = {...doorStyles.value, backgroundColor: '#e5e5'}
    } else {
      puertaLabel.value = 'Puerta cerrada'
      doorStyles.value = {...doorStyles.value, backgroundColor: '#ee5'}
    }
  })
  

</script>

<template>
  <div :style="doorStyles">
    <p>{{puertaLabel}}</p>
    <button @click="open = !open">{{puertaCondition}}</button>
  </div>
</template>

<style>

</style>