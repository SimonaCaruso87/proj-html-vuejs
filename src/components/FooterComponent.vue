<script>

import { store } from '../store.js';

export default{
    name: "FooterComponent",
    data(){
        return{
         store ,
         linkNavbar:[
            { 
                text: "Home",
            },
            {
                text: "Who we are" ,
            },
            {
                text: "What we do" , 
            },
            {
                text: "Where we work",
            },
            {
                text: "Careers",
            },
            {
                text: "News",
            },
            {
                text: "Get In Touch Now",
            },
            
          ],
        }
    },
    methods:{


    }
}
</script>

<template>

    <footer>
        <div>
            <img src="../assets/img/logo_seo_1x.png" alt="logo">
        </div>
        <div class=" container d-flex justify-content-center align-items-center nav-b-footer">
            <ul v-for="(link , i ) in linkNavbar" :key="i" class="navbar-nav menu d-inline-block text-secondary-emphasis">
    <!-- Array element menu -->        
                    <li class="nav-item">
                        <a class="nav-link active font-size p-4" aria-current="page" href="#">{{ link.text }}</a>
                    </li>  
            </ul>
        </div>

    </footer>

</template>

<style lang="scss" scoped>

footer{
    padding:40px;
    text-align: center;

    img{
        width: 100px;
        object-fit: cover;
    }

    .font-size{
        font-size: 12px;
    }

    nav-b-footer:hover{
        background-color:#071B50;
    }
}

</style>