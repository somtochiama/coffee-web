<template>
    <v-row class="email-section" dark>
        <v-col data-aos="fade-up" data-aos-offset="0" class="d-flex flex-column align-center justify-center">
            <h2 class="main-text my-2 display-1">Would you like to hear from us?</h2>
            <p>Submit your email address for our newletter</p>
            <input type="text" placeholder="yourname@mail.com">
        </v-col>
    </v-row>
</template>

<script>
export default {
    
}
</script>

<style scoped>
    h2.main-text {
        font-family: "Lora", sans-serif !important;
    }

    .email-section {
        padding: 5rem;
        color: white;
        background: #2d2e33;
    }

    input[type="text"] {
        border-bottom: 1px solid white;
        padding: 1rem 4rem;
        outline: none;
    }
</style>

