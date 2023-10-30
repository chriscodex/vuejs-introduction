
<script setup lang="ts">
  import { computed, ref, watch } from 'vue';
  const puertaLabel = ref('Puerta cerrada')
  const openDoor = ref(false)
  
  const swapColor = computed(() => {
    return openDoor ? {'open': true,'closed': false } : {'close': false, 'closed': true}
  })

  const buttonDoor = computed(() => {
    return openDoor ? 'Abrir' : 'Cerrar'
  })

  watch(openDoor, (newValue) => {
    if (newValue) {
      puertaLabel.value = 'Puerta abierta'
    } else {
      puertaLabel.value = 'Puerta cerrada'
    }
  })
  

</script>

<template>
  <div :class="{'open': openDoor, 'closed': !openDoor}">
  <!-- <div :class="swapColor"> -->
    <p>{{puertaLabel}}</p>
    <button @click="openDoor = !openDoor">{{buttonDoor}}</button>
  </div>
</template>

<style>
.open {
  background-color: #e5e5;
  color: white;
}

.closed {
  background-color: #ee5;
  color:black;
}
</style>