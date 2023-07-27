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

    <section class="section-two container">
        <div class="text-center fs-4 fw-bold m-5 text-black">What Our Client Say</div>
        <div id="carouselExampleDark" class="carousel carousel-dark slide">
            <div class="carousel-indicators">
                <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="0" class="active button-circle" aria-current="true" aria-label="Slide 1"></button>
                <button type="button" data-bs-target="#carouselExampleDark" data-bs-slide-to="1" class="button-circle" aria-label="Slide 2"></button>
                <button type="button" data-bs-target="#carouselExampleCaptions" data-bs-slide-to="2" class="button-circle" aria-label="Slide 3"></button>

            </div>
            <div class="carousel-inner height">
                <div class="carousel-item active profile-pic  d-flex justify-content-center">
                    <img src="../assets/img/testimonials-1.jpg" class="d-block w-100" alt="testimonials">
                </div>
                <div class="carousel-caption d-none d-md-block">
                    <h5>First slide label</h5>
                    <p>Luis De Salvo CREO TECH</p>
                </div>
                <div class="carousel-item profile-pic  d-flex justify-content-center">
                    <img src="../assets/img/testimonials-2.jpg" class="d-block w-100" alt="testimonials">
                </div>
                <div class="carousel-caption d-none d-md-block">
                    <h5>Second slide label</h5>
                    <p>Some representative placeholder content for the second slide.</p>
                </div>
                <div class="carousel-item height profile-pic d-flex justify-content-center">
                    <img src="../assets/img/testimonials-1.jpg" class="d-block w-100" alt="...">
                </div>
                <div class="carousel-caption d-none d-md-block">
                        <h5>Third slide label</h5>
                        <p>Some representative placeholder content for the third slide.</p>
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
        <hr class="container">
        <div class="container d-flex justify-content-between container-logo-partners">
            <img src="../assets/img/clients_partner_5-200x202.png" alt="client-partners">
            <img src="../assets/img/clients_partner_6-200x202.png" alt="client-partners">
            <img src="../assets/img/clients_partner_1-200x202.png" alt="client-partners">
            <img src="../assets/img/clients_partner_2-200x202.png" alt="client-partners">
        </div>
        
    </section>

</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

// prima section
.section-one{
    background-color: $second-color-bg;
    height: 800px;

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
//section two
.section-two{

    height: 400px;
    .profile-pic{
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #0CD977;
    height: 100px;
    width: 100px;
    overflow: hidden;
    border-radius: 50%;
}

.container-logo-partners{
    height: 200px;
    width: 1000px;
    padding: 50px;
  }

.height{
    height: 250px;
    display: flex;
    justify-content: center;
    padding-right: 70px;
}

.button-circle{
    border-radius: 50%;
    height: 10px;
    width: 10px;
}

}
</style>