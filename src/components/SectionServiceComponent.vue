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
        <div class="text-center text-white pt-5">
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
                <h6 class="p-3 fw-bold">{{ texts.textTitle}}</h6>
                <h6 class="font-size">{{ texts.text }}</h6>
                <h6 class="text-warning font-size pt-4">{{ texts.textBottom }}</h6>
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

}

</style>