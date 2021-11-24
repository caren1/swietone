<template>
  <Layout>
    <Navbar />
    <Home />
    <About />
    <Menu />
  </Layout>
</template>

<script>
import Layout from "./components/Layout.vue";
import Navbar from "./components/Navbar.vue";
import Menu from "./components/Menu.vue";
import Home from "./components/Home.vue";
import About from "./components/About.vue";

export default {
  components: { Navbar, Menu, Home, About, Layout },
};
</script>
