<script>

import { store } from '../store.js';
import ButtonComponent from './ButtonComponent.vue';

export default{
    name: "HeaderComponent",
    components:{
        ButtonComponent
    },
    data(){
        return{
          store,
          linkNavbar:[
            { 
                text: "Home",
                button: false 
            },
            {
                text: "Who we are" ,
                button: false
            },
            {
                text: "What we do" , 
                button: false
            },
            {
                text: "Where we work",
                button: false
            },
            {
                text: "Careers",
                button: false
            },
            {
                text: "APPLY",
                button: true
            },
            {
                text: "News",
                button: false
            },
            
          ],
        }

    },
    methods:{

    }
}
</script>

<template>
    <!-- Container Navbar -->
    <header class="position-relative">
        <div class="container d-flex d-flex-end p-3">
    <!-- Navbar -->    
            <div class="logo"><img src="../assets/img/logo_seo_1x.png" alt="Logo"></div>
    <!-- Menu Navbar -->    
            <ul class="navbar-nav menu d-inline-block text-light navbar-hover">
    <!-- Array element menu -->        
                <template v-for="(link , i ) in linkNavbar" :key="i">
                    <li v-if="link.button == false" class="nav-item">
                        <a class="nav-link active" aria-current="page" href="#">{{ link.text }}</a></li> 
                    <li v-else>
                        <button class="btn btn-outline-warning fs-button" type="button">{{ link.text }}</button>
                    </li>  
                </template>
    <!-- Button Component -->            
                <li><ButtonComponent :textButton="'GET IN TOUCH NOW'"/></li>
            </ul>
        </div>
    <!-- Text Header position absolute -->
        <div class="position-absolute coordinates">
            <h1 class="text-header-bottom">SEM Campaigns Made</h1>
            <h1 class="text-header-bottom">Simple With Avada</h1>
            <h5 class="text-header pt-4">Lorem ipsum dolor, sit amet consectetur</h5>
            <h5 class="text-header pe-4">adipisicing elit. Error, eum!</h5>
    <!-- Button Component + Button Header position absolute -->    
            <div>
                <ButtonComponent :textButton="'BUY AVADA NOW'"/>
                <button class="btn button-blue blue rounded-5 m-4 fw-bold" type="button">CONTACT US</button> 
            </div>
        </div>
    </header>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;


header{
        background-image: url(../assets/img/1-hero-image.png);
        background-repeat: no-repeat;
        background-size: cover;
        height: 850px;       

        .logo{
            margin-right: auto;
            padding: 20px 0px;
        }

        .menu li{
            display: inline-block;
            padding: 20px 20px;

            transition: all 0.1s ease;
        }
        .menu li:hover{
            color:$fourth-color-text;
        }
        .navbar-hover:hover{
            background-color: #001061a2;

            transition: all 1s ease-in-out;
        }
        .fs-button{
            font-size: 11px;
            width: 50px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
        }

        .button-blue.blue:hover{
            background-color:$second-color-bg;
            color: $second-color-button;

            transition: all 0.5s ease-in-out;
        }

        .coordinates{
            top:300px;
            left:300px;
        }

        .text-header{
            color:$fifth-color-button;
        }
        .text-header-bottom{
            color: $fifth-color-button;
            font-weight: bolder;
        }
}

</style>