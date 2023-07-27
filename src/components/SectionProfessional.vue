<script>

import { store } from '../store.js';


export default{
    name: "SectionOurNewsComponent",
    
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
                    <div class="carousel-caption d-none d-md-block">
                        <h5>First slide label</h5>
                        <p>Luis De Salvo CREO TECH</p>
                    </div>
                </div>
                
                <div class="carousel-item profile-pic  d-flex justify-content-center">
                    <img src="../assets/img/testimonials-2.jpg" class="d-block w-100" alt="testimonials">
                    <div class="carousel-caption d-none d-md-block">
                    <h5>Second slide label</h5>
                    <p>Some representative placeholder content for the second slide.</p>
                </div>
                </div>
                
                <div class="carousel-item height profile-pic d-flex justify-content-center">
                    <img src="../assets/img/testimonials-1.jpg" class="d-block w-100" alt="...">
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


template{
    
}
// prima section
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
    height: 50px;
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