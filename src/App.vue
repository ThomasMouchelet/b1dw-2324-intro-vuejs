<script setup>
import { ref } from 'vue'
import CardItemsList from './components/CardItemsList.vue';

const cardItemsList = ref([
  {
    id: 999,
    titel: "Card test"
  }  
])

</script>

<template>
  <h1>App component</h1>

  <nav>
    <RouterLink to="/">Go to Home</RouterLink>
    <RouterLink to="/about">Go to About</RouterLink>
  </nav>

  <RouterView />

  <CardItemsList></CardItemsList>
</template>