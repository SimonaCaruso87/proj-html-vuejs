<script>

import { store } from '../store.js';


export default{
    name: "SectionConsultation",
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
    <section>
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black pt-2">
            <h4 class="fw-bold">Start Your Free Consultation</h4>
            <h6 class="font-size">Sed ud perspicitis dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6 class="font-size">tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container">
        <!-- Numero 6 Card in array -->
        </div>   
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    height: 300px;
    background-image: url(../assets/img/case-study-gallery-3-1-800x600.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    opacity: rgba(0, 0, 0, 0.527);
    width: 100%;

}

</style>