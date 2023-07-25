<script>

import { store } from '../store.js';

export default{
    name: "MainComponent",
    data(){
        return{
          store,
          textMain:[
            { 
                textTitle: "Establish Goals",
                text: "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.",
                fontAwesome : "fa-solid fa-road"
            },
            { 
                textTitle : "Work With A Team",
                text : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.",
                fontAwesome : "fa-solid fa-video"
            },
            { 
                textTitle : "Get Results",
                text : "Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.",
                fontAwesome : "fa-solid fa-droplet"
            },
           ] 
        }
    },

    methods:{

    }
}
</script>

<template>
    <main class="pt-5">
        <!-- Title Main Section Bottom -->
        <div class="container text-center">
            <h3 class="text-black fw-bold">Meet The New Agency SEO Template</h3>
            <h3 class="text-black fw-bold">From The Avada Team</h3>
            <h6 class="pt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam</h6>
            <h6>ut explicabo ratione!</h6>
        </div>
        <!-- Card Section Central -->
        <div class="container w-100 d-flex justify-content-center align-items-center">
            <!-- Card 1 Establich Goals -->
            <div v-for="(texts , i ) in textMain" :key="i" class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <div class="d-flex justify-content-center align-items-center p-2" style="color:orange;"><font-awesome-icon :icon="texts.fontAwesome"/></div>
                <a href="#"><h5 class="fw-bold text-center change p-2">{{ texts.textTitle }}</h5></a>
                <h6 class="font-size text-center">{{ texts.text }}</h6>
            </div>
        </div>
            <!-- Img Footer -->
        <div class="d-flex justify-content-center align-items-center" style="width: 100%;">
            <img src="../assets/img/agency-seo-desk-front-800x380.jpg" style="width:800px; height:380px; border:1px solid #f8f8f8;" alt="desk-front">
        </div>
        
    </main>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

main{
    background-color:$second-color-bg;
    height:auto;

    .font-size{
        color: $third-color-text;
        font-size: $third-size;
        padding: 5px;
        word-spacing: 4px;
    }
    .change:hover{
        color:$fourth-color-text;
    }
    a{
        text-decoration: none;
    }
}

</style>