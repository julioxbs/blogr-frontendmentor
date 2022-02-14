<template>
  <Header />
  <Designed />
  <Art />
  <FreeOpen />
  <Footer />
</template>

<script>
import Header from "./components/Header.vue";
import Designed from "./components/Designed.vue";
import Art from "./components/Art.vue";
import FreeOpen from "./components/FreeOpen.vue";
import Footer from "./components/Footer.vue";
export default {
    components: {
        Header, 
        Designed,
        Art, FreeOpen,
        Footer,
    }
}
</script>