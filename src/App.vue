<template>
  <Layout>
    <Navbar />
    <Home />
    <About />
  </Layout>
</template>

<script>
import Layout from "./components/Layout.vue"
import Navbar from "./components/Navbar.vue";
import Home from "./components/Home.vue";
import About from "./components/About.vue";

export default {
  components: { Navbar, Home, About, Layout },
};
</script>
