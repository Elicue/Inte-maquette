<template>
  <Header/>
</template>

<script>
import Header from '@/components/header.vue'

export default {
  name: 'HomeView',
  components: {
    Header,
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: 'Poppins', sans-serif;
  text-decoration: none;
}

body {
  background-color: black;
}
</style>
