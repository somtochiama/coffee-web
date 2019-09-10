<template>
    <v-row class="text-center">
        <v-col>
            <h2 class="text-uppercase">#Noansacoffee</h2>
            <p>Coffee perfection since 1927</p>
        </v-col>
        <div class="gallery">
            <div v-for="n in 12" :key="n" class="img-box">
                <img :src="`gallery/${n}.jpg`" />
            </div>
        </div>
    </v-row>
</template>


<style scoped>

h2 {
    font-size: 36px;
}

.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fill, minmax(200px, 1fr));
    grid-auto-rows: 200px
}

.img-box img {
    height: 100%;
    width: 100%;
    object-fit: cover;
}
    
</style>