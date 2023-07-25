<script>

import { store } from '../store.js';

export default{
    name: "MainSectionServiceComponent",
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
    <section class="p-5">
        <!-- Title Section Main Component Service -->
        <div class="text-center text-white pt-5">
            <h4>See Our Top Noth Service</h4>
            <h6>Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6>tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container text-center d-flex justify-content-center align-items-center p-3">
        <!-- Card 1 -->
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <i class="fa-brands fa-google" style="color:orange; display: block; height: 50px;"></i>
                <h5>Google SEO</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 2 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <i class="fa-solid fa-gear" style="color:orange; display: block; height: 50px;"></i>
                <h5>Brand Strategy</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 3 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <i class="fa-solid fa-building" style="color:orange; display: block; height: 50px;"></i>
                <h5>Local SEO</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 4 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <i class="fa-solid fa-chart-bar" style="color:orange; display: block; height: 50px;"></i>
                <h5>SEO Analysis</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    background-color: $first-color-bg;
    height: 600px;
    background-image: url(../assets/img/pattern_background.png);
    background-repeat: no-repeat;

    .container-card{
        background-color: $third-color-bg;
        color: $fifth-color-button;        
    }

    .font-size{
       font-size: 11px;
       word-spacing: 4px;
    }

}

</style>