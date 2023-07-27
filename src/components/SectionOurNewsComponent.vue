<script>

import { store } from '../store.js';
import ButtonComponent from './ButtonComponent.vue';


export default{
    name: "SectionOurNewsComponent",
    components:{
        ButtonComponent
    },
    data(){
        return{ 
          store ,
          imgArray:[
            {
              textImg:"../assets/img/related-service-4-700x441.jpg"

            },
            {
              textImg:"../assets/img/related-service-2-700x441.jpg"

            },
            {
              textImg:"../assets/img/blog-post-6-700x441.jpg"

            },
           ],
           textArray:[
            {
               textTitle:"Why You Need a SEO Agency Now" ,
               textDate: " November 1st , 2017" ,
               text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Deserunt, dolorem exercitationem modi ullam maxime delectus ad corporis id doloremque fugit."
            },   
            {
               textTitle:"SEO Tips For Your Startup" ,
               textDate: " November 1st , 2017" ,
               text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Deserunt, dolorem exercitationem modi ullam maxime delectus ad corporis id doloremque fugit."
            },   
            {
               textTitle:"Image Optimization For Your Site" ,
               textDate: " November 1st , 2017" ,
               text:"Lorem, ipsum dolor sit amet consectetur adipisicing elit. Deserunt, dolorem exercitationem modi ullam maxime delectus ad corporis id doloremque fugit."
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
    <div>
        
    </div>
    <section class="section-one p-5">
        <!-- Title Section Main Component Our Work -->
        <div class="text-center text-black p-2">
            <h4 class="fw-bold">Our News</h4>
            <h6 class="font-size">Lorem ipsum dolor sit amet consectetur adipisicing elit. In accusamus</h6>
            <h6 class="font-size">tempore laboriosam minus!</h6>
        </div>
        <!-- Container Card -->
        <div class="container size" style="width: 1300px;">
        <!-- Numero 6 Card in array -->
            <div v-for="(image , i) in imgArray" :key="i" class="card container-card m-2" style="height:250px; width:320px; border:0px;">
                <img :src="getImgPath(image.textImg)" alt="blog-post" class="h-100 object-fit-cover">
            </div>
            <div v-for="(textsArray , i) in textArray" :key="i" class="card container-card m-2" style="height:200px; width:320px; border:0px; background-color:#f8f8f8 ;">
                <h6 class="text-warning fw-bold pt-2">{{ textsArray.textTitle }}</h6>
                    <div class="text-secondary-emphasis font-size ">{{ textsArray.textDate }}</div>
                    <div class="fs-7">{{ textsArray.text }}</div>
            </div>
        </div>
        <div class="d-flex justify-content-center pb-1">
            <ButtonComponent style="width:140px ; height:40px; font-size: 10px;" :textButton="'GO TO NEWS'"/>
        </div>
    </section>

    
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;


template{
    background-color: $second-color-bg;
    height: 800px;
}
// prima section
.section-one{

    

    .font-size{
       font-size: 10px;
    }

    .fs-7{

        font-size: 12px;
        padding: 10px;
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