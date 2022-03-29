<template>
  <div id="app">
    <Header />

    <main>
      <Products />
    </main>

    <footer>
      <Footer />
    </footer>
  </div>
</template>

<script>
import Header from './components/Header.vue'
import Products from './components/Products.vue'
import Footer from './components/Footer.vue'


export default {
  components: {
    Header,
    Products,
    Footer
  }
}
</script>

<style lang="scss">

@import "./assets/scss/style.scss";

</style>
