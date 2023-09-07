<template>
  <div>
    <Navbar />
    <HeroImage />
    <About />
    <Gallery />
    <Footer />
  </div>
</template>

<script>
import About from './sections/About.vue';
import Footer from './sections/Footer.vue';
import Gallery from './sections/Gallery.vue';
import HeroImage from './sections/HeroImage.vue';
import Navbar from './sections/Navbar.vue';

export default {
  components: {
    HeroImage,
    About,
    Footer,
    Navbar,
    Gallery,
  },
}
</script>

<style lang="scss">
#app {
  font-family: 'Montserrat', sans-serif;
  h1 {
    font-size: 48px;
    letter-spacing: 8px;
  }
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  overflow: auto;
}
body {
  margin: 0%;
}
</style>
