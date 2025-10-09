<template>
  <div class="app">
    <h1>谁最美丽可爱</h1>
    <Person />
  </div>
</template>

<script lang="ts">
import Person from './components/Person.vue'
export default {
  name: 'App',
  components: { Person }
}
</script>

<style>
.app {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
button{
  margin: 0 5px;
}
</style>