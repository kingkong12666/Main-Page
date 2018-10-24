<template>
  <v-app>
    <header>
      <div class="headerContent">
        <img
          class="share"
          src="./image/Logo_layer.png"
        >
        <sapn class="phone">+971 56 437 7612</sapn>
      </div>
    </header>


    <div class="menuItem">
      <v-menu
        bottom
        origin="center center"
        transition="scale-transition"
      >
        <v-btn
          slot="activator"
          class="logo"
        >Logo</v-btn>
        <v-btn
          slot="activator"
        >
          Company
        </v-btn>
        <v-btn
          slot="activator"
        >
          Products
        </v-btn>
        <v-btn
          slot="activator"
        >
          Service
        </v-btn>
        <v-btn
          slot="activator"
        >
          Portfolio
        </v-btn>
        <v-btn
          slot="activator"
        >
          News
        </v-btn>
        <v-btn
          slot="activator"
        >
          Contacts
        </v-btn>

      </v-menu>

    </div>
    <v-container fluid grid-list-sm>
    <v-layout>
      <v-flex>
        <v-carousel hide-controls>
          <v-carousel-item
            v-for="item in carouselItems"
            :src="require(`./image/${item.src}`)"
          >
            <div class="carouselContent">
              <span>The Best Company</span>
              <p class="target">to Help Your Business</p>
              <p class="description">International leader in the design, manufacture and installation of complete equipment for the retail sector</p>
            </div>
          </v-carousel-item>
        </v-carousel>
      </v-flex>
    </v-layout>

      <h1>Products</h1>
      <v-layout>
        <v-flex
          v-for="item in productItems"
          xs6 sm4>
          <v-img
            :src="require(`./image/${item.src}`)"
          >
            <div class="productContent">
              <p class="font-weight-light">{{item.title}}</p>
            </div>
          </v-img>
        </v-flex>
      </v-layout>
      <v-layout row wrap text-xs-center grid-list-md style="margin-top: 40px">
        <v-flex v-for="item in infoItems"  xs6>
          <v-img
            class="px-0"
            :src="require(`./image/${item.src}`)"

          >
            <div class="infoContent">
              <p class="infoTitle font-weight-light">{{item.title}}</p>
            </div>
          </v-img>
        </v-flex>
      </v-layout>
    </v-container>

    <header>
      <div class="headerContent">

        <sapn class="copy font-weight-light">&copy; Solution for retail. All rights reserved</sapn>
        <span class="footer font-weight-light">LEGAL | SITEMAP | CONTACTS</span>
      </div>
    </header>


  </v-app>
</template>

<script>

export default {
  data () {
    return {
      carouselItems: [
        {
          src: 'mainPhoto.png'
        },
        {
          src: 'mainPhoto.png'
        },
        {
          src: 'mainPhoto.png'
        }
      ],
      infoItems: [
        {
          src: 'portfolio.png',
          title: 'Portfolio'
        },
        {
          src: 'portfolio.png',
          title: 'About'
        }
      ],
      productItems: [
        {
          src: 'pic1.png',
          title: 'Remote'
        },
        {
          src: 'pic2.png',
          title: 'Plug-in'
        },
        {
          src: 'pic3.png',
          title: 'Non Refrigerated Cabinets'
        },
        {
          src: 'pic4.png',
          title: 'Hot-Cases'
        },
        {
          src: 'pic5.png',
          title: 'Refrigeration Systems'
        }
      ]
    }
  },
  name: 'App',
  components: {
  }
}
</script>
<style>
  .footer{
    color: white;
    font-size: 14px;
    position: relative;
    float: right;
    margin-right: 135px;
  }
  .copy{
    color: white;
    font-size: 14px;
    position: relative;
    font-family: Roboto,sans-serif;
  }
  .infoTitle{
    color: white;
    font-size: 48px;
  }
  .infoContent{
    position: relative;
    top: 40%;
    display: table;
    width: 100%;
  }
  .infoTitle{
    vertical-align: middle;
  }

  .productContent > p {
    color: white;
    font-size: 12px;
    text-align: center;
    vertical-align: middle;
    display: table-cell;
    font-family: Roboto,sans-serif;
  }
  .productContent{
    background-color: rgba(0,0,0,.5);
    height: 90px;
    position: relative;
    top: 58%;
    display: table;
    width: 100%;
  }
  h1{
    color: #002258;
  }
  .container.fluid {
    position: relative;
    margin-left: 135px;
    margin-right: 135px;
    padding: 0;
    max-width: 80%;
  }
  .description {
    color: white;
    font-size: 13px;
    margin-left: 80px;

  }
  .carouselContent {
    background-color: rgba(0,0,0,.5);
    height: 170px;
    position: relative;
    top: 30%;

  }
  .target {
    font-size: 43px;
    color: white;
    margin-left: 80px;
    margin-bottom: 0;
  }
  .carouselContent > span {
    font-size: 51px;
    color: white;
    margin-left: 80px;
  }
  .v-carousel__controls{
    background: none;
  }
  .v-carousel{
    width: 100%;
    margin-top: 15px;
  }
  header{
    background-color: #002258;
    width: 100%;
    height: 40px;
  }
  .share{
    position: relative;
    top: 7px;
  }
  .phone{
    color: white;
    font-size: 14px;
    position: relative;
    left: 45px;
  }
  .headerContent{
    margin-left: 135px;
  }


  .v-btn{
    color: #002258;
    vertical-align: middle;
    display: table-cell;
    font-size: 13px;
    margin-right: 28px;
  }
  .theme--light.v-btn:not(.v-btn--icon):not(.v-btn--flat){
    background-color: #fff;

  }
  .theme--light.application{
    background-color: #fff;
  }
  .v-btn:not(.v-btn--depressed):not(.v-btn--flat){
    box-shadow: none;
  }
  .logo{
    width: 285px;
    height: 85px;
    border: 1px solid #002258;
    text-align: center;
    font-size: 30px;
    position: relative;
  }
  .menuItem{
    width: 100%;
    margin-left: 127px;
    position: relative;
    top: 10px;
  }
</style>
