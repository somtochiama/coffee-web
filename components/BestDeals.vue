<template>
    <v-content class="pb-12 px-12" id="deals">
        <v-row>
            <v-col class="main-text">
                <p data-aos="fade-up" class="small-text">Buy Now</p>
                <h2 data-aos="fade-up" class="my-2">Our Best Deals</h2>
                <p data-aos="fade-up" class="mission">Coffee company with a straightforward mission: to make an office and on-the-go cup of coffee that we like to drink ourselves</p>
            </v-col>
        </v-row>
        <v-row>
            <v-col md="4" data-aos="fade-down" v-for="item in coffee" :key="item.level">
                <div class="img">
                    <img src="../assets/product.png">
                </div>
                <div class="text" data-aos="fade-up" data-aos-duration="1500">
                    <p class="small-text">{{item.level}}</p>
                    <p class="name">{{item.name}}</p>
                    <ShopBtn :small="true" :text="item.price"/>
                </div>
            </v-col>
        </v-row>
    </v-content>
</template>

<script>
import ShopBtn from "~/components/ShopBtn";

export default {
    data: () => ({
        coffee: [
            { 
                img: "", 
                level: "platinium", 
                name: "Noansa Platinium Blend",
                price: "$30.00"
            },
            { 
                img: "", 
                level: "classic",
                name: "Noansa Classic Blend",
                price: "$30.00"
            },
            { 
                img: "", 
                level: "general", 
                name: "Noansa Classic Blend",
                price: "$10.00"
            }
        ]
    }),
    components: {
        ShopBtn
    }
}
</script>

<style scoped>

    @import url("../assets/styles/text.css");

    h2 {
        font-size: 28px;
    }

    #deals {
        background: #fffcee;
        text-align: center;
        /* padding: 6rem 4rem */
    }

    img {
        width: 100%;
    }

    .main-text {
        padding: 7rem 3rem 4rem;
        margin: 0;
        background: linear-gradient(rgba(255, 252, 238, 0.8), rgba(255, 252, 238, 0.8)),  url("../assets/icons/doodle.svg");
        background-repeat: no-repeat;
        background-position: center;
    }

    .text {
        display: flex;
        justify-content: center;
        flex-direction: column;
        align-items: center;
        text-transform: capitalize;
    }

    p.mission {
        font-size: 20px;
    font-weight: 300;
    max-width: 40rem;
    margin: auto;
    }
</style>