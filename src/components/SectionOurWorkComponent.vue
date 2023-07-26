<script>

import { store } from '../store.js';

export default{
    name: "SectionOurWorkComponent",
    data(){
        return{
          store ,
          imgArray:[
            {
              textImg:" "

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
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black fw-bold pt-3">
            <h4>Our Work</h4>
            <h6>Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6>tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container text-center d-flex flex-wrap justify-content-center align-items-center p-3" style="width: 1300px;">
        <!-- Numero 6 Card in array -->
            <div class="card container-card m-3 " style="height:250px; width:300px;">
                <img src="../assets/img/case-study-gallery-1-1-600x450.jpg" alt="blog-post" class="h-100 object-fit-cover">
            </div>
        </div>
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    background-color: $second-color-bg;
    height: 600px;

    .font-size{
       font-size: 11px;
       word-spacing: 4px;
    }

    .font-section{
        color:orange; 
        display: block; 
        height: 50px;
    }

}

</style>