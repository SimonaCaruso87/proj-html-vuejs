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

    <button class="btn button-white white rounded-5">{{ textButton }}</button>
    
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

        
        .button-white.white{
            height: 30px;
            display:flex;
            justify-content: center;
            align-items: center;

            transition: all 1s ease-in-out;
        }

        .button-white.white:hover{
            background-color:$first-color-button;
            color:$fifth-color-button;
            border: none;

        }

        
</style>