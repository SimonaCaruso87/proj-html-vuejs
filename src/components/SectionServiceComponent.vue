<script>

import { store } from '../store.js';

export default{
    name: "SectionServiceComponent",
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
                <div class="d-flex justify-content-center align-items-center p-2 text-warning"><font-awesome-icon icon="fa-brands fa-google"/></div>
                <h6 class="p-2 fw-bold">Google SEO</h6>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning font-size pt-2">Read More > </h6>
            </div>
        <!-- Card 2 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <div class="d-flex justify-content-center align-items-center p-2 text-warning"><font-awesome-icon icon="fa-solid fa-gear"/></div>
                <h6 class="p-2 fw-bold">Brand Strategy</h6>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning font-size pt-2">Read More > </h6>
            </div>
        <!-- Card 3 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <div class="d-flex justify-content-center align-items-center p-2 text-warning"><font-awesome-icon icon="fa-solid fa-building"/></div>
                <h6 class="p-2 fw-bold">Local SEO</h6>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning font-size pt-2">Read More > </h6>
            </div>
        <!-- Card 4 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:200px;">
                <div class="d-flex justify-content-center align-items-center p-2 text-warning"><font-awesome-icon icon="fa-solid fa-chart-bar"/></div>
                <h6 class="p-2 fw-bold">SEO Analysis</h6>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning font-size pt-2">Read More > </h6>
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
       font-size: 10px;
       word-spacing: 4px;
    }

}

</style>