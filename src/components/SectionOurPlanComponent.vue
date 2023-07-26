<script>

import { store } from '../store.js';
import ButtonComponentWhite from './ButtonComponentWhite.vue';


export default{
    name: "SectionOurPlanComponent",
    components:{
        ButtonComponentWHite ,
    },
    data(){
        return{ 
          store ,
          plan:[
            {
               typePlan : "Standard",
               pricePlan: 19,
               projectPlan: "5 Projects",
               storagePlan: "5 GB Storage",
               userPlan: "Unlimited Users" ,

            },
            {
               typePlan : "Premium",
               pricePlan: 29,
               projectPlan: "10 Projects",
               storagePlan: "10 GB Storage ",
               userPlan: "Unlimited Users" ,

            },
            {
               typePlan : "Professional",
               pricePlan: 39,
               projectPlan: "15 Projects",
               storagePlan: "15 GB Storage",
               userPlan: "Unlimited Users" ,

            },
            {
               typePlan : "Extreme",
               pricePlan: 59,
               projectPlan: "Unlimited Projects",
               storagePlan: "Unlimited Storage",
               userPlan: "Unlimited Users" ,

            },
          ]
          
        }
    },
    methods:{
        
    }
}
</script>

<template>
    <section class="p-5">
        <!-- Title Section Main Component Our Plans -->
        <div class="text-center text-white">
            <h4 class="fw-bold">Our Plans</h4>
            <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6 class="font-size">tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container size" style="width: 1300px;">
        <!-- Numero 4 Card in array -->
            <div v-for="(plans , i) in plan" :key="i" class="container-card m-2 p-3 bg-white position-relative" style="height:300px; width:200px;">
                <h5 class="fw-bold">{{ plans.typePlan }}</h5>
                <div><h1><span class="text-black fs-7 position-absolute fw-bold">&dollar;</span><span class="text-primary fs-1">{{  plans.pricePlan }}</span><span class="fs-12 text-black fw-bold">monthly</span><span class="fs-6 position-absolute coordinates text-primary">00</span></h1></div>
                <div class="text-color p-3">{{ plans.projectPlan }}</div>
                <div class="text-color p-3">{{  plans.storagePlan }}</div>
                <div class="text-color p-3">{{  plans.userPlan }}</div>
        <!-- Button Section -->        
                <div class="d-flex justify-content-center align-items-center">
                    <ButtonComponentWhite :textButton="'START TODAY'"/>
                </div>
            </div>
        </div>
        
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    background-image: url(../assets/img/background1.jpg);
    background-repeat: no-repeat;
    background-size: cover;
    height: 600px;

    .font-size{
       font-size: 12px;
    }

    .fs-12{
        font-size:$first-size;
    }
    .fs-7{
        font-size:$fourth-size;
        vertical-align: top;

        top:60px;
        left:55px;
    }

    .text-color{
        color:$third-color-text;
        font-weight: bold;
        font-size: $fourth-size;

    }

    // .font-section{
    //     color:orange; 
    //     display: block; 
    //     height: 50px;
    // }
    
    .size{
        text-align: center; 
        display:flex; 
        flex-wrap: wrap; 
        justify-content:center; 
        align-items:center; 
        padding:15px;
    }

    .coordinates{
        top:60px;
        left:106px;
    }

}

</style>