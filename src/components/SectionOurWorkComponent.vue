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
        <div class="text-center text-black pt-2">
            <h4 class="fw-bold">Our Work</h4>
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
        <div class="d-flex justify-content-center pt-3 pb-5">
            <ButtonComponent style="width:140px ; height:40px; font-size: 10px;" :textButton="'VIEW OUR WORK'"/>
        </div>
    </section>
    <section>
        <div id="carouselExampleDark" class="carousel carousel-dark slide">
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Slide 1"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" aria-label="Slide 2"></button>
    <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="2" aria-label="Slide 3"></button>
  </div>
  <div class="carousel-inner">
    <div class="carousel-item active" data-bs-interval="10000">
      <img src="..." class="d-block w-100" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5>First slide label</h5>
        <p>Some representative placeholder content for the first slide.</p>
      </div>
    </div>
    <div class="carousel-item" data-bs-interval="2000">
      <img src="..." class="d-block w-100" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5>Second slide label</h5>
        <p>Some representative placeholder content for the second slide.</p>
      </div>
    </div>
    <div class="carousel-item">
      <img src="..." class="d-block w-100" alt="...">
      <div class="carousel-caption d-none d-md-block">
        <h5>Third slide label</h5>
        <p>Some representative placeholder content for the third slide.</p>
      </div>
    </div>
  </div>
  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="prev">
    <span class="carousel-control-prev-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Previous</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#carouselExampleDark" data-bs-slide="next">
    <span class="carousel-control-next-icon" aria-hidden="true"></span>
    <span class="visually-hidden">Next</span>
  </button>
</div>
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    background-color: $second-color-bg;
    height: 800px;

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