<script>

import { store } from '../store.js';
import ButtonComponent from './ButtonComponent.vue';


export default{
    name: "SectionOurWorkComponent",
    components:{
        ButtonComponent
    },
    data(){
        return{ 
          store ,
          imgArray:[
            {
              textImg:"../assets/img/case-study-gallery-3-1-600x450.jpg"

            },
            {
              textImg:"../assets/img/case-study-gallery-2-600x450.jpg"

            },
            {
              textImg:"../assets/img/case-study-gallery-1-1-600x450.jpg"

            },
            {
              textImg:"../assets/img/case-study-gallery-4-1-600x450.jpg"

            },
            {
              textImg:"../assets/img/case-study-gallery-5-1-600x450.jpg"

            },
            {
              textImg:"../assets/img/case-study-gallery-6-1-600x450.jpg"

            },
          ]
        }
    },
    methods:{
        getImgPath:(imgSrc) => {
            return new URL(imgSrc,
            import.meta.url).href;
        },
    }
}
</script>

<template>
    <section class="p-5">
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black pt-3">
            <h4 class="fw-bold" >Our Work</h4>
            <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6 class="font-size">tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container size" style="width: 1300px;">
        <!-- Numero 6 Card in array -->
            <div v-for="(image , i) in imgArray" :key="i" class="card container-card m-2" style="height:250px; width:320px; border:0px;">
                <img :src="getImgPath(image.textImg)" alt="blog-post" class="h-100 object-fit-cover">
            </div>
        </div>
        <div class="d-flex justify-content-center p-4" >
            <ButtonComponent :textButton="'VIEW OUR WORK'"/>
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
       font-size: 12px;
    }

    .font-section{
        color:orange; 
        display: block; 
        height: 50px;
    }
    
    .size{
        text-align: center; 
        display:flex; 
        flex-wrap: wrap; 
        justify-content:center; 
        align-items:center; 
        padding:15px;
    }
}

</style>