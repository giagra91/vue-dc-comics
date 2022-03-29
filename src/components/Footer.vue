<template>
  <div class="home-footer">
    <div id="footer-top">
      <div id="top-footer-wrapper">
        <div id="top-footer-links">
          <div class="pad-1">
            <h4>Dc comics</h4>
            <ul>
              <li v-for="(element, index) in comicsLinks" :key="index">
                <a :href="element.url">
                  {{element.text}}
                </a>
              </li>
            </ul>
            <h4>Dc comics</h4>
            <ul>
              <li v-for="(element, index) in shopLinks" :key="index">
                <a :href="element.url">
                  {{element.text}}
                </a>
              </li>
            </ul>
          </div>
          <div class="pad-1">
            <h4>Dc</h4>
            <ul>
              <li v-for="(element, index) in dcLinks" :key="index">
                <a :href="element.url">
                  {{element.text}}
                </a>
              </li>
            </ul>
          </div>
          <div class="pad-1">
            <h4>Sites</h4>
            <ul>
              <li v-for="(element, index) in sitesLinks" :key="index">
                <a :href="element.url">
                  {{element.text}}
                </a>
              </li>
            </ul>
          </div>
        </div>
        <div id="top-footer-image">
          <!-- <img src="../assets/images/dc-logo-bg.png" alt="Dc logo"> -->
        </div>
      </div>

    </div>
    <div id="footer-bottom">
      <div id="footer-bottom-wrapper">
        <div id="footer-subscription">
          <a href="#">
            Sign-up Now!
          </a>
        </div>
        <div id="footer-follow-us">
          <h3>Follow us</h3>
          <a href="#" class="mar-2">
            <img src="../assets/images/footer-facebook.png" alt="Facebook logo">
          </a>
          <a href="#" class="mar-2">
            <img src="../assets/images/footer-twitter.png" alt="Twitter logo">
          </a>
          <a href="#" class="mar-2">
            <img src="../assets/images/footer-youtube.png" alt="Youtube logo">
          </a>
          <a href="#" class="mar-2">
            <img src="../assets/images/footer-pinterest.png" alt="Pinterest logo">
          </a>
          <a href="#" class="mar-2">
            <img src="../assets/images/footer-youtube.png" alt="Periscope logo">
          </a>
        </div>

      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'HomeFooter',
  data: function(){
    return {
        comicsLinks: [
        {
          text: `Characters`,
          url: `#`,
        },
        {
          text: `Comics`,
          url: `#`,
        },
        {
          text: `Movies`,
          url: `#`,
        },
        {
          text: `Tv`,
          url: `#`,
        },
        {
          text: `Games`,
          url: `#`,
        },
        {
          text: `Videos`,
          url: `#`,
        },
        {
          text: `News`,
          url: `#`,
        },
      ],
      dcLinks: [
        {
          text: `Terms of Use`,
          url: `#`,
        },
        {
          text: `Privacy Policy (New)`,
          url: `#`,
        },
        {
          text: `Ad Choices`,
          url: `#`,
        },
        {
          text: `Advertising`,
          url: `#`,
        },
        {
          text: `Jobs`,
          url: `#`,
        },
        {
          text: `Subriscpitons`,
          url: `#`,
        },
        {
          text: `Talent Workshops`,
          url: `#`,
        },
        {
          text: `CPSP Certificates`,
          url: `#`,
        },
        {
          text: `Ratings`,
          url: `#`,
        },
        {
          text: `Shop Help`,
          url: `#`,
        },
        {
          text: `Contact Us`,
          url: `#`,
        },
      ],
      sitesLinks: [
        {
          text: `DC`,
          url: `#`,
        },
        {
          text: `MAD Magazine`,
          url: `#`,
        },
        {
          text: `DC Kids`,
          url: `#`,
        },
        {
          text: `DC Universe`,
          url: `#`,
        },
        {
          text: `DC Power Visa`,
          url: `#`,
        },
      ],
      shopLinks: [
        {
          text: `Shop DC`,
          url: `#`,
        },
        {
          text: `Shop DC Collectibles`,
          url: `#`,
        },
      ],
    }
    
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="scss" scoped>
@import "../assets/scss/partials/variables.scss";

div#footer-top{
  width: 100%;
  height: 42vh;
  background-image: url("../assets/images/footer-bg.jpg");

  div#top-footer-wrapper{
    width: 80%;
    height: 100%;
    margin: 0 auto;
    padding: 0 1rem;
    display: flex;
    justify-content: space-between;
    color: white;

    div#top-footer-links{
      width: 50%;
      display: flex;

      h4{
        text-transform: uppercase;
        padding: .9rem 0;
      }
  
      ul{
        list-style-type: none;
  
  
        a{
          text-decoration: none;
          color: grey;
          font-size: .7rem;

          &:hover{
            color: white;
          }
        }
      }
    }

    div#top-footer-image{
      width: 40%;
      height: 100%;
      background-image: url("../assets/images/dc-logo-bg.png");
      background-position: center;
      background-size: cover;
    }
  }
}

.pad-1{
  padding: 0 .8rem;
}

.mar-2{
  margin: 0 .4rem;
}

div#footer-bottom{
  width: 100%;
  height: 14vh;
  background-color: #303030;

  div#footer-bottom-wrapper{
    width: 80%;
    height: 100%;
    margin: 0 auto;
    padding: 0 1rem;
    display: flex;
    justify-content: space-between;
    align-items: center;

    div#footer-subscription{
      
      a{
        text-decoration: none;
        color: white;
        text-transform: uppercase;
        padding: .7rem;
        font-size: .8rem;
        font-weight: bold;
        border: 2px solid $BrandColor;
      }
    }

  div#footer-follow-us{
    height: 100%;
    display: flex;
    align-items: center;

    h3{
      text-transform: uppercase;
      font-weight: bold;
      padding: 0 1rem;
      font-size: 1rem;
      color: $BrandColor;
    }
  }

  }
}
</style>
