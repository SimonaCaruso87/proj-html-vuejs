<script>

import { store } from '../store.js';


export default{
    name: "HeaderComponent",
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

    <header class="position-relative">
        <div class="container d-flex d-flex-end p-3">
            <div class="logo"><img src="../assets/img/logo_seo_1x.png" alt="Logo"></div>
            <ul class="navbar-nav menu d-inline-block text-light">
                <li class="nav-item"><a class="nav-link active" aria-current="page" href="#">Home</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Who we are</a></li>
                <li class="nav-item"><a class="nav-link" href="#">What we do</a></li>
                <li class="nav-item"><a class="nav-link" href="#">Where we work</a></li>
                <li class="nav-item pe-0"><a class="nav-link" href="#">Careers</a></li>
                <li><button class="btn btn-outline-warning fs-button" type="button">APPLY</button></li>
                <li><a class="nav-link active" aria-current="page" href="#">News</a></li>
                <li><button class="btn button-orange orange rounded-5 fs-orange" type="button">GET IN TOUCH NOW</button></li>
            </ul>
        </div>
        <div class="position-absolute coordinates">
            <h1 class="text-header-bottom">SEM Campaigns Made</h1>
            <h1 class="text-header-bottom">Simple With Avada</h1>
            <h5 class="text-header pt-4">Lorem ipsum dolor, sit amet consectetur</h5>
            <h5 class="text-header pe-4">adipisicing elit. Error, eum!</h5>
            <button class="btn button-orange orange fs-button-bottom rounded-5 m-4" type="button">BUY AVADA NOW</button>
            <button class="btn button-blue blue fs-button-bottom rounded-5 m-4" type="button">CONTACT US</button> 
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
        }

        .menu li{
            display: inline-block;
            padding: 0 20px;
        }
        .menu li:hover{
            color:$fourth-color-text;
        }
        .fs-button{
            font-size: 11px;
            width: 50px;
            height: 30px;
            display: flex;
            justify-content: center;
            align-items: center;
        }
        .fs-orange{
            font-size: 12px ;
            color: white;
            font-weight: bolder;
            padding: 15px;
        }
        .fs-button-bottom{
            font-size: 12px ;
            color: white;
            font-weight: bolder;
            padding: 15px;
            width:200px;
            font-weight: bolder;
        }
        .fs-orange:hover{
            background-color:orangered;
        }

        .coordinates{
            top:300px;
            left:300px;
        }

        .text-header-bottom{
            color:white;
            font-weight: bolder;
        }
        .text-header{
            color:white;
        }
}

</style>