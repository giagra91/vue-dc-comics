<template>
  <div class="home-header">
    <div id="header-container">
      <img src="../assets/images/dc-logo.png" alt="DC logo">
      <nav >
        <ul>
          <li v-for="(link,index) in links" :class="{active: link.visible}" :key="index" @click="changeActiveLink(index)">
            <a :href="link.url" :class="{active: link.visible}">{{link.text}}</a>
          </li>
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeHeader',
  data: function(){
    return {
      links: [
        {
          text: `Characters`,
          url: `#`,
          visible: true
        },
        {
          text: `Comics`,
          url: `#`,
          visible: false
        },
        {
          text: `Movies`,
          url: `#`,
          visible: false
        },
        {
          text: `Tv`,
          url: `#`,
          visible: false
        },
        {
          text: `Games`,
          url: `#`,
          visible: false
        },
        {
          text: `Collectibles`,
          url: `#`,
          visible: false
        },
        {
          text: `Videos`,
          url: `#`,
          visible: false
        },
        {
          text: `Fans`,
          url: `#`,
          visible: false
        },
        {
          text: `News`,
          url: `#`,
          visible: false
        },
        {
          text: `Shop`,
          url: `#`,
          visible: false
        },
      ]
    }
  },
  methods: {
    changeActiveLink(activeIndex){
      console.log(activeIndex)
      this.links.forEach((element, index) => {
        if (activeIndex === index){
          element.visible = true;
        } else {
          element.visible = false;
        }
      })
    },
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
div.home-header{
  width: 80%;
  height: 14vh;
  margin: 0 auto;

  div#header-container{
    height: 100%;
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 0 1rem;

    img{
      height: 70%;
    }

    nav{
      height: 100%;
      line-height: 100px;

      ul{
      height: 100%;
      list-style-type: none;
      display: flex;

        li{
          height: 100%;
          padding: 0 .3rem;
          text-transform: uppercase;
          font-size: .8rem;
          cursor: pointer;

          &:hover,
          &.active{
            border-bottom: 5px solid #0c7cec;
          }
          a{
            text-decoration: none;
            font-weight: bold;
            color: #575757;

              &.active,
              &:hover{
              color: #0c7cec;
              }
          }
        }
      }
    }
  }
}
</style>
