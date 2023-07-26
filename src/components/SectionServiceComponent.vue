<script>

import { store } from '../store.js';

export default{
    name: "SectionServiceComponent",
    data(){
        return{
          store ,
          textArray : [
            {
                fontAwesomeIcon:"fa-brands fa-google",
                textTitle:"Google SEO" ,
                text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.",
                textBottom: "Read More > "
            },
            {
                fontAwesomeIcon:"fa-solid fa-gear",
                textTitle:"Brand Strategy" ,
                text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.",
                textBottom: "Read More > "
            },
            {
                fontAwesomeIcon:"fa-solid fa-building",
                textTitle:"Local SEO" ,
                text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.",
                textBottom: "Read More > "
            },
            {
                fontAwesomeIcon:"fa-solid fa-chart-bar",
                textTitle:"SEO Analysis" ,
                text:"Lorem ipsum dolor sit amet consectetur adipisicing elit. Cum corporis saepe minima earum quasi laudantium exercitationem reiciendis commodi nesciunt tempore.",
                textBottom: "Read More > "
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
        <!-- Title Section Main Component Service -->
        <div class="text-center text-white p-2">
            <h4>See Our Top Noth Service</h4>
            <h6>Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6>tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container container-section">
        <!-- Numero 4 Card in Array -->
            <div 
            v-for="(texts, i) in textArray" 
            :key="i" 
            class="card container-card m-3 p-3" 
            style="height:300px; width:200px;">
                <div class="fontawesome-style"><font-awesome-icon :icon="texts.fontAwesomeIcon"/></div>
                <h6 class="p-3 fw-bold change">{{ texts.textTitle}}</h6>
                <h6 class="font-size">{{ texts.text }}</h6>
                <a href="#"><h6 class="text-warning font-size pt-4 visible">{{ texts.textBottom }}</h6></a>
                <a href="#"><h6 class="font-size component-visible">Let's Work Togheter ></h6></a>
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

    .container-section{
        text-align:center;
        display:flex; 
        justify-content:center; 
        align-items:center; 
        padding:20px;
    }

    .container-card{
        background-color: $third-color-bg;
        color: $fifth-color-button;  
        border:10px solid $third-color-bg;

        transition: all 0.3s ease-in-out;
    }

    .container-card:hover{
        background-color: $third-color-bg;
        border:10px solid #092369;

    }

    .container-card:hover .change{
        color: $fourth-color-text;

    }

    .fontawesome-style{
        display:flex;
        justify-content:center; 
        align-items:center;
        padding:10px;
        color:$fourth-color-text;
    }

    .font-size{
       font-size: 12px;
       word-spacing: 4px;
    }

    .component-visible{
     padding-top: 24px 0px 0px;
     visibility: hidden;
     opacity: 0;
     color: $fourth-color-text;
    }

    .visible{
        position: relative;
    }
    .container-card:hover .visible{
      visibility: hidden;
      opacity:0;
    }

    .container-card:hover .component-visible{
        opacity: 1;
        visibility: visible;
        position: absolute;
        bottom:2px;
        left:30px;
    }

    a{
        text-decoration: none;
    }
}   


</style>