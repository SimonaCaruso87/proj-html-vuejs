<script>

import { store } from '../store.js';
import WorkCardComponent from './WorkCardComponent.vue';



export default{
    name: "SectionProfessional",
    
    data(){
        return {
            testimonialList:[
                {
                    linkImg:'../assets/img/testimonials-1.jpg',
                    text:'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Assumenda pariatur aut id possimus cupiditate vel!',
                    name:'Lorem ipsum',
                    society:'sit amet'
                },     
                {
                    linkImg:'../assets/img/testimonials-2.jpg',
                    text:'Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience',
                    name:'luis desalvo',
                    society:'creo tech'
                },     
                {
                    linkImg:'../assets/img/testimonials-1.jpg',
                    text:'Ability proceeds from a fusion of skills, knowledge, understanding and imagination, consolidated by experience',
                    name:'luis desalvo',
                    society:'creo tech'
                },     
            ],
            testimonialActive:0,
        }
    },
    components:{
        WorkCardComponent
    },
    methods:{
        getImgPath: (imgSrc)=> {
            return new URL(imgSrc, import.meta.url).href;
        },
        cangeTestimonialActive(index){
            this.testimonialActive = index;
        }
    }
}
</script>

<template>
    <section id="testimonials">
        <div class="container">
           <h4 class="fw-bold text-center" >What our clients say</h4>
            <div class="slider">
                <template v-for="(testimonial, index) in testimonialList" :key="index">
                    <div class="testimonial" v-if="index == testimonialActive">
                        <div class="img-wrapper">
                            <img :src="getImgPath(testimonial.linkImg)" :alt="testimonial.name">
                        </div>
                        <p class="text">{{ testimonial.text }}</p>
                        <p>
                            <span class="name">{{ testimonial.name }}</span>,
                            <span class="society">{{ testimonial.society }}</span>
                        </p>
                    </div>
                </template>
                <div class="comand-slider">
                    <div class="bullet" 
                        :class="index == testimonialActive ? 'active' : ''" 
                        v-for="(testimonial, index) in testimonialList" 
                        :key="index"
                        @click="cangeTestimonialActive(index)"
                    >
                    </div>
                </div>
            </div>
            <!--end slider-->
        </div>
    </section>
    <!--end vantage section-->
</template>

<style lang="scss" scoped>

    @use '../assets/scss/partials/mixins.scss' as *;
    @use '../assets/scss/partials/variables.scss' as *;

    #testimonials{
        padding-block: 50px;
        h2{
            text-align: center;
            text-transform: capitalize;
        }

        .slider{
            border-bottom: 1px solid #d0d3dd; 
            padding-bottom: 50px;    
            .testimonial{
                text-align: center;
                .img-wrapper{
                    width: 150px;
                    height: 150px;
                    border-radius: 50%;
                    margin-inline: auto;
                    overflow: hidden;
                    margin-block: 50px;
                    background-size: cover;
                }
                p{
                    &.text{
                        max-width: 600px;
                        margin-inline: auto;
                        line-height: 150%;
                        font-style: italic;
                        font-weight: 500;
                        margin-bottom: 30px;
                    }
                    span{
                        &.name{
                            font-weight: 700;
                            text-transform: capitalize;
                        }
                        &.society{
                            text-transform: uppercase;
                            font-weight: 500;
                        }
                    }
                        
    
                }
                
                
    
            }
    
            .comand-slider{
                display: flex;
                align-items: center;
                justify-content: center;
                margin-block:30px;
                gap: 10px;
                .bullet{
                    width: 20px;
                    height: 20px;
                    border: 1px solid black;
                    border-radius: 50%;
                    cursor: pointer;
                    &.active{
                        background-color: black;
                    }
                }
            }
        }
    }
</style>