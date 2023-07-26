<script>

import { store } from '../store.js';


export default{
    name: "ButtonComponentWhite",
    data(){
       
        return{
          store 
        }

    },
    methods:{

    },
    props:{
        textButton:{
            type:String,
            default:""
        },

    }
}
</script>

<template>

    <button class="d-flex justify-content-center align-items-center button-white white">{{ textButton }}</button>
    
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;



        .button-white.white:hover{
            background-color:$first-color-bg;
            color:$fifth-color-button;
            border: none;

            transition: all 0.5s ease-in-out;
        }

        
</style>