<script>

import { store } from '../store.js';
import SectionServiceComponent from './components/SectionServiceComponent.vue';
import SectionOurWorkComponent from './components/SectionOurWorkComponent.vue';

export default{
    name: "MainComponent",
    components:{
        SectionServiceComponent ,
        SectionOurWorkComponent ,
    },
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
        <!-- Title Main Section Top -->
        <div class="container text-center">
            <h3 class="text-black fw-bold">Meet The New Agency SEO Template</h3>
            <h3 class="text-black fw-bold">From The Avada Team</h3>
            <h6 class="pt-3">Lorem ipsum dolor sit amet consectetur adipisicing elit. Aperiam</h6>
            <h6>ut explicabo ratione!</h6>
        </div>
        <!-- Container Card Section Central -->
        <div class="container w-100 d-flex justify-content-center align-items-center">
        <!-- Numero Card 3 in Array -->
            <div 
            v-for="(texts , i ) in textMain" :key="i" 
            class="bg-white p-4 m-4" 
            style="height: 250px; width: 300px;">
                <div class="container-card"><font-awesome-icon :icon="texts.fontAwesome"/></div>
                <a href="#"><h5 class="fw-bold text-center change p-2">{{ texts.textTitle }}</h5></a>
                <h6 class="font-size text-center fw-bold">{{ texts.text }}</h6>
            </div>
        </div>
        <!-- Img Bottom -->
        <div class="img-container">
            <img 
            src="../assets/img/agency-seo-desk-front-800x380.jpg" 
            class="img-bottom" 
            alt="desk-front">
        </div>

        <SectionServiceComponent />

        <SectionOurWorkComponent />
        
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
        font-size: $fourth-size;
        padding: 10px;
        word-spacing: 10px;
    }

    .container-card{
        display:flex;
        justify-content:center; 
        align-items:center; 
        padding:10px;
        color:$fourth-color-text;
    }

    .change{
        color:black;
    }
    .change:hover{
        color:$fourth-color-text;
    }
    a{
        text-decoration: none;
    }

    .img-container{
        display:flex; 
        justify-content:center;
        align-items:center; 
        width: 100%;
    }

    .img-bottom{
        width:800px; 
        height:380px; 
        border:1px solid #f8f8f8;
    }
}

</style>