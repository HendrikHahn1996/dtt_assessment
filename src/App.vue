<template>
  <div id="app">
    <router-view />
  </div>
</template>

<script>

import Home from '@/views/Home.vue'
export default {
  name: 'app',
  components: {
    Home
  }

}

</script>

<style>
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0; 
  background-color: rgb(246, 246, 246);;
}

</style>
