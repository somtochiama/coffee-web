<template>
    <v-row class="additional">
        <v-col 
            md="3"
            v-for="card in cards"
            :key="card.img"
            flat 
            :class="['info-section', {'active': card.active}]"
        >
        <v-card class="section" flat>
          <div class="icon pl-6 pt-12 pb-3">
            <img :src="card.img" />
          </div>
          <v-card-text class="short-text pt-3 pb-8 px-5">
            {{card.text}}
          </v-card-text>
        </v-card>
      </v-col>
    </v-row>
</template>

<script>
import Leaf from "~/assets/icons/leaf.svg";
import Log from "~/assets/icons/log.svg";
import Tulip from "~/assets/icons/tulip.svg";
import Flower from "~/assets/icons/flower.svg";
export default {
    data: () => ({
        cards: [
            { img: Leaf, text: "Quality Coffee cultivated by good", active: true},
            { img: Log, text: "Quality Coffee cultivated by good", active: false},
            { img: Tulip, text: "Quality Coffee cultivated by good", active: false},
            { img: Flower, text: "Quality Coffee cultivated by good", active: false},
        ]
    })
}
</script>

<style scoped>

/* .icon {

} */
.additional {
  padding: 4rem 7rem;
}

.info-section {
    background: none
}

.info-section.active .section{
    border-top-right-radius: 2rem;
    background: #fff0ca;
}

.info-section.active .icon {
    background: #ffcf59;
    border-top-right-radius: 2rem;
    border-bottom: 20%;
    border-bottom-left-radius: 40%;
    border-bottom-right-radius: 40%;
}

.icon > img {
  height: 30px;
  width: 30px;
}

.info-section {
  padding: 6rem 3rem
}

.short-text {
    font-weight: 500;
    font-size: 22px;
    color: black !important;
    text-transform: capitalize;
    line-height: 1.2;
}
    
</style>