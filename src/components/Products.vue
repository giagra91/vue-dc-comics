<template>
  <div>
    <div class="products-wrapper">
      <div id="products">
        <a id="current-series" href="#">Current Series</a>
        <ProductCard 
        v-for="(element, index) in ProductsContent" :key="index" :gameElement="element" />
        <a id="load-series" href="#">Load more</a>
      </div>
    </div>
    <div id="products-links">
      <div id="links-to-shop">
        <div class="single-link" v-for="(element, index) in ShopContents" :key="index">
          <img :src="require(`@/assets/images/` + element.img)" :alt="element.text">
          <p>{{ element.text }}</p>
        </div>
      </div>
    </div>

  </div>
</template>

<script>

import ProductCard from "./ProductCard.vue"
export default {
  name: 'HomeProducts',
  components: {
    ProductCard,
  },
  data: function(){
    return {
      ProductsContent: [
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/AC1000_DLX_162-001_HD_5ba13723281ab0.37845353.jpg?itok=ZsI-C5eX",
        "price": "$19.99",
        "series": "Action Comics",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/AV1976_01_300-001_HD_5f738f6e39ddd7.18205602.jpg?itok=VgdYdJ01",
        "price": "$3.99",
        "series": "American Vampire 1976",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2018/08/AQMv4_UW_153-001_HD_5b7efa1745a9b8.08589135.jpg?itok=HPTtnrsb",
        "price": "$16.99",
        "series": "Aquaman",
        "type": "graphic novel"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/06/batgirl_v5_1_5b23e1f1124941.50950783.jpg?itok=VnrJah76",
        "price": "$2.99",
        "series": "Batgirl",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
        "price": "$3.99",
        "series": "Batman",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2018/09/BM_56_300-001_HD_5ba137a85c3bf3.33122291.jpg?itok=3FHJQYJZ",
        "price": "$2.99",
        "series": "Batman Beyond",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2019/08/BMSM_5d4361b7116261.74371456.jpg?itok=kEDR2OL8",
        "price": "$3.99",
        "series": "Batman/Superman",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMSMANN_01_300-001_HD_5f5ff17fa1d665.74704970.jpg?itok=azz5sfGk",
        "price": "$4.99",
        "series": "Batman/Superman Annual",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/09/BMTJWZ_01_300-001_HD_5f5ff2307dcb37.34652945.jpg?itok=VswVjLR8",
        "price": "$5.99",
        "series": "Batman: The Joker War Zone",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/08/cover-v2_5f40314645a734.37285065.png?itok=ImNM2QBY",
        "price": "$6.99",
        "series": "Batman: Three Jokers",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/comic-covers/2020/10/BMWK_HQ_01_300-001_HD_5f7cb4945e13f6.89501032.jpg?itok=sVwALbUX",
        "price": "$4.99",
        "series": "Batman: White Knight Presents: Harley Quinn",
        "type": "comic book"
      },
      {
        "thumb": "https://www.dccomics.com/sites/default/files/styles/covers192x291/public/gn-covers/2019/04/CTWv1_CC_144-001_HD_5ca5299a751963.53054221.jpg?itok=ooPaoLDq",
        "price": "$16.99",
        "series": "Catwoman",
        "type": "graphic novel"
      }
    ],
    ShopContents: [
      {
        img: "buy-comics-digital-comics.png",
        text: "Digital Comics"
      },
      {
        img: "buy-comics-merchandise.png",
        text: "Dc Merchandise"
      },
      {
        img: "buy-comics-subscriptions.png",
        text: "Subscription"
      },
      {
        img: "buy-comics-shop-locator.png",
        text: "Comic Shop Locator"
      },
      {
        img: "buy-dc-power-visa.svg",
        text: "Dc Power Visa"
      },
    ]
    }
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" >
@import "../assets/scss/partials/variables.scss";

.text-center{
  text-align: center;
}

div.products-wrapper{
  width: 100%;
  // height: 14vh;
  background-color: #1c1c1c;
    div#products{
      width: 80%;
      height: 100%;
      margin: 0 auto;
      padding: 2rem 1rem;
      color: white;
      display: flex;
      justify-content: center;
      flex-wrap: wrap;
      align-items: center;
      position: relative;
        
        a{
        width: 150px;
        background-color: $BrandColor;
        padding: .6rem 0;
        text-align: center;
        text-decoration: none;
        color: white;
        text-transform: uppercase;
        font-size: .8rem;
        font-weight: bold;
        }
        a#load-series{
          margin-top: 2rem;

        }
        a#current-series{
          position: absolute;
          left: 3%;
          top: -3%;
        }

    }
}
    div#products-links{
      width: 100%;
      height: 16vh;
      background-color: #0282f9;

      div#links-to-shop{
        width: 75%;
        height: 100%;
        margin: 0 auto;
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;

        div.single-link{
          height: 100%;
          margin: 0 .8rem;
          display: flex;
          align-items: center;

          img{
            height: 35%;
          }

          p{
            text-transform: uppercase;
            margin-left: .5rem;
            font-weight: bold;
            font-size: .8rem;
          }
        }


      }
    }

</style>
