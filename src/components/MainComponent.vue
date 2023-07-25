<script>

import { store } from '../store.js';

export default{
    name: "MainComponent",
    data(){
        return{
          store
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
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <i class="fa-solid fa-road fa-2xl" style="color:orange; display: block; height: 50px;"></i> 
                <a href="#"><h5 class="text-black fw-bold text-center change">Establish Goals</h5></a>
                <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>
            </div>
            <!-- Card 2 Work With a Team -->
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <i class="fa-solid fa-video 2-xs" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="text-black fw-bold text-center change">Work With A Team</h5>
                <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>

            </div>
            <!-- Card 3 Get Results -->
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <i class="fa-solid fa-droplet" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="text-black fw-bold text-center change">Get Results</h5>
                <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>

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
}

</style>