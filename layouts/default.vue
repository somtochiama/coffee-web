<template>
  <v-app id="main">
    <!-- <v-container id="box"> -->
      <nuxt />
    <!-- </v-container> -->
  </v-app>
</template>

<script>
export default {
  data () {
    return {
      clipped: false,
      drawer: false,
      fixed: false,
      items: [
        {
          icon: 'mdi-apps',
          title: 'Welcome',
          to: '/'
        },
        {
          icon: 'mdi-chart-bubble',
          title: 'Inspire',
          to: '/inspire'
        }
      ],
      miniVariant: false,
      right: true,
      rightDrawer: false,
      title: 'Vuetify.js'
    }
  }
}
</script>

<style scoped>
  #box {
    margin: 0;
    padding: 0;
  }

  #main {
    font-family: 'Lora', serif;
    background-color: white;
  }
</style>
