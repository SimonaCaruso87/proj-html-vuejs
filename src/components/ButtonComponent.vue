<script>

import { store } from '../store.js';


export default{
    name: "ButtonComponent",
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
    
    <button class="btn button-orange  orange rounded-5" type="button">{{ textButton }}</button>
    

</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

        .button-orange.orange:hover{
            background-color:$second-color-bg;
            color:$first-color-button;
            border: none;

            transition: all 0.5s ease-in-out;
        }

        
</style>