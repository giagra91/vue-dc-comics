<template>
  <div>
    <div class="products-wrapper">
      <div id="products">
        <h2>--> Content goes here -- 
        </h2>
      </div>
    </div>
    <div id="products-links">
      <div id="links-to-shop">
        <h2>Prova</h2>
      </div>
    </div>

  </div>
</template>

<script>
export default {
  name: 'HomeProducts',
  data: function(){
    return {
      
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
div.products-wrapper{
  width: 100%;
  height: 100px;
  background-color: #1c1c1c;
    div#products{
      width: 80%;
      height: 100%;
      margin: 0 auto;
      padding: 0 1rem;
      color: white;
      display: flex;
      align-items: center;
    }
}
    div#products-links{
      width: 100%;
      height: 120px;
      background-color: #0282f9;

      div#links-to-shop{
        width: 75%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        align-items: center;
      }
    }

</style>
