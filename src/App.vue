<template>
  <div class="app">
    <h1>你好啊！</h1>
  </div>

  <Person />
  <Car/>
</template>

<script lang="ts">
import Car from './components/Car.vue';
import Person from './components/Person.vue';

export default {
  name: 'App', //组件名

  components: { Person, Car }
}
</script>

<style>
.app {
  background-color: #ddd;
  box-shadow: 0 0 10px;
  border-radius: 10px;
  padding: 20px;
}
</style>
