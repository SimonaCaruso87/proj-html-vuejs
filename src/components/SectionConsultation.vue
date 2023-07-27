<script>

import { store } from '../store.js';
import ButtonComponentWhite from './ButtonComponentWhite.vue';



export default{
    name: "SectionConsultation",
    components:{
        ButtonComponentWhite
    },
    data(){
        return{ 
          store ,
        }
    },
    methods:{
       
    }
}
</script>

<template>
    <section class="position-relative">
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black p-4 position-absolute cont-text text-white">
            <h4 class="fw-bold p-2">Start Your Free Consultation</h4>
            <h6 class="font-size p-2">Sed ud perspicitis dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6 class="font-size p-2">tempore laboriosam minus!</h6>
            <ButtonComponentWhite  class="but-white text-white" style="width: 130px;" :textButton="'CONTACT US NOW'"/>
        </div>
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    height: 400px;
    background-image: url(../assets/img/CTA-seo-1.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    width: 100%;

    .cont-text{
        top: 50%;
        left: 50%;
        transform: translate(-50%,-50%);
    }

    .but-white{
        position: absolute;
        left:245px;
        background-color:$first-color-button;
        color:third-color-button;
        border:none;
    }
    .but-white:hover{
        background-color: $third-color-button;
        color:$first-color-button;
    }

}

</style>