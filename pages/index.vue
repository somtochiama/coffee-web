<template>
  <v-content >
    <Banner />
    <InfoSection />
    <QualityCoffee />
    <BestDeals />
    <QualityCoffee />
    <Gallery />
    <ContactForm />
    <Footer />
  </v-content>
</template>

<script>
import Banner from "~/components/Banner.vue"
import InfoSection from "~/components/InfoSection.vue";
import QualityCoffee from "~/components/QualityCoffee.vue";
import BestDeals from "~/components/BestDeals.vue";
import Gallery from "~/components/Gallery.vue";
import ContactForm from "~/components/ContactForm.vue";
import Footer from "~/components/Footer.vue"

export default {
  components: {
    Banner,
    InfoSection,
    QualityCoffee,
    BestDeals,
    Gallery,
    ContactForm,
    Footer
  }
}
</script>

<style scoped>

/* .before-section {
  content: url("../assets/icons/blur.svg");
  position: relative;
  z-index: 50;
  right: 0px
}
   */
</style>svg
