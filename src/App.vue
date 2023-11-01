<script setup lang="ts">
import HelloWorld from './components/HelloWorld.vue';
import UserEvents from './components/UserEvents.vue';
import ReactiveInput from './components/ReactiveInput.vue';
import ComputeProperties from './components/ComputeProperties.vue';
import Watcher from './components/Watcher.vue';
import DinamicStyles from './components/DinamicStyles.vue';
import DinamicStyles2 from './components/DinamicStyles2.vue';
import Condicionales from './components/Condicionales.vue';
import MultipleRender from './components/MultipleRender.vue';
import ParentComponent from './components/caseComponent/ParentComponent.vue';
import RaizComponent from './components/slotExample/RaizComponent.vue';
import ParenComp from './components/comunicationParentChild/ParentComp.vue';
import ParentComp from './components/comunicationChildParent/ParentComp.vue';
import ParentC from './components/modelChildParent/ParentC.vue';
const msgg = 'message for test';
const htmVariable = '<h1>Hello World</h1>';
const urlImageTest =
  'https://images.pexels.com/photos/268533/pexels-photo-268533.jpeg?cs=srgb&dl=pexels-pixabay-268533.jpg&fm=jpg';
</script>

<template>
  <h1>{{ msgg }}</h1>
  <h1 v-text="msgg"></h1>
  <h1 v-once v-html="htmVariable"></h1>
  <HelloWorld msg="message" />
  <!-- Atributo reactivo -->
  <img :src="urlImageTest" />

  <UserEvents />
  <ReactiveInput />
  <h3>Propiedades Computadas</h3>
  <ComputeProperties />
  <h3>Watcher</h3>
  <Watcher />
  <h3>Dinamic Styles</h3>
  <DinamicStyles />
  <h3>Dinamic Styles 2</h3>
  <DinamicStyles2 />
  <h3>Condicionales</h3>
  <Condicionales />
  <h3>Multiple Render</h3>
  <MultipleRender />
  <h3>Multiple Components - Child & Parent</h3>
  <ParentComponent />
  <h3>Slot</h3>
  <RaizComponent />
  <h3>Comunication</h3>
  <h4>Parent - Son</h4>
  <ParenComp />
  <h4>Son - Parent</h4>
  <ParentComp />
  <h4>Model Son - Parent</h4>
  <ParentC />
</template>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}
</style>
