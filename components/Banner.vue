<template>
    <v-row class="box">
      <v-col md="5" class="right">
          <v-toolbar flat class="nav">
          <v-toolbar-items data-aos="fade-left" class="pa-0">
            <v-btn text>Logo</v-btn>
          </v-toolbar-items>
          </v-toolbar>
          <div data-aos="fade-up" class="small-text mt-8">Prenium Coffee</div>
          <h1 data-aos="fade-up" class="main-text  my-2">A cup of pleasant coffee is one of the most important pleasures in life.</h1>
          <ShopBtn data-aos="fade-up" />
      </v-col>
      <v-col data-aos="fade-left" md="7" id="banner">
        <v-card flat>
          <v-toolbar flat class="nav d-flex justify-center">
          <v-toolbar-items>
            <v-btn  
              v-for="link in links"
              :key="link"
              data-aos="fade-left"  
              text
            >{{link}}</v-btn>
            <img data-aos="fade-left" class="mr-3" src="../assets/icons/search.svg" />
            <img data-aos="fade-left" class="ml-3" src="../assets/icons/user.svg" />
          </v-toolbar-items>
          </v-toolbar>
        </v-card>
      </v-col>
    </v-row>
</template>

<script>
import ShopBtn from "~/components/ShopBtn.vue";

export default {
  data: () => ({
    links: ["Shop", "Wholesale", "Location", "Our Story"]
  }),
  components: {
    ShopBtn
  }
}
</script>

<style scoped>
  .box {
  background: #F2EFE3;
}

.nav {
  background: none !important;
}

.nav  img {
  width: 20px;

}

.right {
  background: linear-gradient(rgba(243, 240, 228, 0.8), rgba(243, 240, 228, 0.8)), url("../assets/icons/doodle.png");
  background-repeat: no-repeat;
  background-position: top left;
  /* background-color: #f3f0e4; */
  padding-left: 7em;
}

h2.text {
  line-height: 1;
  font-weight: 500;
  margin: 20px 0;
  font-weight: 300;
  font-size: 15px !important;
}

.small-text {
  text-transform: uppercase;
  font-weight: 400;
  line-height: 0.2rem;
  font-size: 15px !important;
}

#banner {
  background-image: url("../assets/banner.png");
  background-position: top right;
  background-size: cover;
  height: 35rem;
}

#banner > * {
  background: none;
}
</style>