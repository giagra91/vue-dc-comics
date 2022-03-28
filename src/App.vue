<template>
  <div id="app">
    <Header />

    <main>
      <Products />
    </main>

    <Footer />
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

<style>
*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
#app {
}
</style>
