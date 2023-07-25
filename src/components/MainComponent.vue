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
    <main class="p-5">
        <div class="container text-center">
            <h3 class="text-black fw-bold">Meet The New Agency SEO Template</h3>
            <h3 class="text-black fw-bold">From The Avada Team</h3>
            <h6 class="pt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam</h6>
            <h6>ut explicabo ratione!</h6>
        </div>
        <div class="container w-100 d-flex justify-content-center align-items-center">
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
             <h5 class="text-black fw-bold text-center">Establish Goals</h5>
             <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>
            </div>
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <h5 class="text-black fw-bold text-center">Work With A Team</h5>
                <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>

            </div>
            <div class="bg-white p-4 m-4" style="height: 200px; width: 250px;">
                <h5 class="text-black fw-bold text-center">Get Results</h5>
                <h6 class="font-size text-center">Lorem ipsum dolor, sit amet consectetur adipisicing elit. Natus eaque rerum accusantium in beatae incidunt? Inventore quas ratione exercitationem suscipit.</h6>

            </div>
        </div>
        <div class="d-flex justify-content-center align-items-center">
            <img src="../assets/img/agency-seo-desk-front-600x285.jpg" style="width:600px; height:285px;" alt="desk-front">
        </div>
    </main>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

main{
    background-color:$second-color-bg;
    height:600px;

    .font-size{
        color: $third-color-text;
        font-size: $third-size;
        padding: 5px;
        word-spacing: 4px;
    }
}

</style>