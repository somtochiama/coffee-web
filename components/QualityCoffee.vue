<template>
    <v-row class="before-section">
        <v-col data-aos="fade-right" lg="6" :class="['img-lap', 'd-flex', 'mt-n12', {reverse: reverse}]">
            <div class="art">
                <img class="dots" src="../assets/icons/blur.svg">
                <div class="img-div">
                    <img src="../assets/plant.jpg" />
                </div>
                <div class="bandaid"></div>
            </div>
        </v-col>
        <v-col data-aos="fade-left" lg="6" class="d-flex align-center">
            <div class="main-text">
                <p class="small-text">Prenium Good Coffee</p>
                <h2 class="mt-3 text-capitalize">Quality Coffee</h2>
                <h2 class="mb-3 text-capitalize">cultivated by good</h2>
                <p class="long-text">Our love for specialty coffee is never-ending. With over 365 days a year at origin working with the best growers on the planet, only the best beens make the grade</p>
                <ShopBtn data-aos="fade-up" />
            </div>
        </v-col>
    </v-row>
</template>

<script>
import ShopBtn from "~/components/ShopBtn.vue"
export default {
    props: {
        reverse: {
            type: Boolean,
            default: false
        }
    },
  components: {
      ShopBtn
  }  
}
</script>

<style scoped>
@import url("../assets/styles/text.css");

.main-text {
  background: linear-gradient(rgba(255, 255, 255, 0.8), rgba(255, 255, 255, 0.8)),  url("../assets/icons/doodle.svg");
  background-repeat: no-repeat;
  background-position-y: -7rem;
  
}

.long-text {
    margin: 10px 0;
    line-height: 1.5;
    margin-right: 3rem;
}


h2 {
    line-height: 1.5;
}

.before-section {
    padding: 7rem 5rem;
}

.img-lap.reverse {
    order: 1;
    transform: rotate(90deg);
    margin-top: 50px !important;
}

.art {
    width: fit-content;
}

/* .before-section::before {
    content: url("../assets/icons/dots.svg");
    height: 200px;
    width: 200px
} */

.bandaid {
    background-color: rgb(255, 207, 89, 0.8);
    width: 180px;
    height: 40px;
    z-index: 4;
    position: relative;
    border-radius: 30px;
    transform: rotate(-45deg);
    left: 20rem;
    bottom: 40px;
}

.img-div {
    z-index: 2;
    position: relative;
    /* position: absolute; */
    left: 5rem;
    top: 1rem;
    width: 350px;
    border-bottom-left-radius: 40%;
    height: 350px;
}

.img-div > img {
    width: 100%;
    height: 100%;
    border-bottom-left-radius: 50%;
    border-top-left-radius: 50%;
    border-top-right-radius: 50%
}

.dots {
    position: absolute;
    z-index: 1;
    height: 200px;
}


</style>