<template>
  <div class="wrapper">
    <Navbar />

  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
export default {
  components: { Navbar }
}
</script>

<style>
  .wrapper {
    width: 100vw;
    height: 100vh;
    text-align: center;
    place-items: center;
    background-color: #0E483E;
    position: relative;
  }
</style>
