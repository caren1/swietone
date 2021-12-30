<template>
  <Layout>
    <div v-if="!isMenuOpen">
      <Navbar @toggleMenu="isMenuOpen = $event" />
      <Home />
      <About />
      <Bio />
      <Logos />
      <Footer />
    </div>
    <div v-else>
      <Menu @toggleMenu="isMenuOpen = $event" />
    </div>
  </Layout>
</template>

<script>
import Layout from "./components/Layout.vue";
import Navbar from "./components/Navbar.vue";
import Menu from "./components/Menu.vue";
import Home from "./components/Home.vue";
import About from "./components/About.vue";
import Logos from './components/Logos/Logos.vue'
import Bio from "./components/Bio.vue";
import Footer from "./components/Footer.vue";

export default {
  components: { Navbar, Menu, Home, About, Layout, Bio, Footer, Logos },
  data() {
    return {
      isMenuOpen: false,
    };
  },
};
</script>
