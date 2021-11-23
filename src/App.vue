<template>
  <div class="wrapper">
    <Navbar />
    <Home />
    <About />
  </div>
</template>

<script>
import Navbar from './components/Navbar.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
export default {
  components: { Navbar, Home, About}
}
</script>

<style>
  .wrapper {
    width: 100vw;
    height: 100%;
    text-align: center;
    place-items: center;
    background-color: #0E483E;
  }
</style>
