<template>
  <div id="app">
    <Header />

    <main>
      <Jumbotron />
      <Products />
    </main>

    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Jumbotron from './components/Jumbotron.vue'
import Products from './components/Products.vue'
import Footer from './components/Footer.vue'


export default {
  components: {
    Header,
    Jumbotron,
    Products,
    Footer
  }
}
</script>

<style lang="scss">

@import "./assets/scss/style.scss";

</style>
