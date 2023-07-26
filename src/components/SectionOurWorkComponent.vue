<script>

import { store } from '../store.js';

export default{
    name: "SectionOurWorkComponent",
    data(){
        return{
          store ,
          textArray:[
            {
              textTitle:" "

            }
          ]
        }
    },
    methods:{

    }
}
</script>

<template>
    <section class="p-5">
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black fw-bold pt-3">
            <h4>Our Work</h4>
            <h6>Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6>tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container text-center d-flex flex-wrap justify-content-center align-items-center p-3" style="width: 1300px;">
        <!-- Card 1 -->
            <div class="card container-card m-3 p-4" style="height:250px; width:300px;">
                <i class="fa-brands fa-google font-section"></i>
                <img src="../assets/img/blog-post-6-700x441.jpg" alt="blog-post" class="w-100">
            </div>
        <!-- Card 2 -->    
            <div class="card container-card m-3 p-4" style="height:250px;width:300px;">
                <i class="fa-solid fa-gear font-section"></i>
                <h5 class="p-2">Brand Strategy</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 3 -->    
            <div class="card container-card m-3 p-4" style="height:250px; width:300px;">
                <i class="fa-solid fa-building" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="p-2">Local SEO</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 4 -->    
            <div class="card container-card m-3 p-4" style="height:250px;width:300px;">
                <i class="fa-solid fa-chart-bar" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="p-2">SEO Analysis</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 5 -->    
            <div class="card container-card m-3 p-4" style="height:250px;width:300px;">
                <i class="fa-solid fa-chart-bar" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="p-2">SEO Analysis</h5>
                <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.</h6>
                <h6 class="text-warning">Read More > </h6>
            </div>
        <!-- Card 6 -->    
            <div class="card container-card m-3 p-4" style="height:250px;width:300px;">
                <i class="fa-solid fa-chart-bar" style="color:orange; display: block; height: 50px;"></i>
                <h5 class="p-2">SEO Analysis</h5>
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
    background-color: $second-color-bg;
    height: 600px;

    .font-size{
       font-size: 11px;
       word-spacing: 4px;
    }

    .font-section{
        color:orange; 
        display: block; 
        height: 50px;
    }

}

</style>