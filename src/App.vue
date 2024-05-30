<script setup>
import { ref } from 'vue'
import CardItemsList from './components/CardItemsList.vue';

const cardItemsList = ref([
  {
    id: 999,
    title: "Card test"
  }  
])

// Add new item to cardItemsList

</script>

<template>
  <h1>App component</h1>

  <nav>
    <RouterLink to="/">Go to Home</RouterLink>
    <RouterLink to="/about">Go to About</RouterLink>
  </nav>

  <div class="container">
    <div class="row">
      <div class="col">
        <RouterView />
      </div>
      <div class="col">
        <CardItemsList title="List items card"></CardItemsList>
      </div>
    </div>
  </div>
</template>

<style scoped>
.row{
  display: flex;
}
.col:nth-of-type(1){
  flex: 4;
}
.col:nth-of-type(2){
  flex: 1;
}
</style>