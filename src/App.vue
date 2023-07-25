<script>

import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ButtonComponent from './components/ButtonComponent.vue';
import MainSectionServiceComponent from './components/MainSectionServiceComponent.vue';
import axios from 'axios';
import { store } from './store.js';


export default{
  name:"App",
  components:{
     HeaderComponent ,
     MainComponent ,
     FooterComponent ,
     ButtonComponent ,
     MainSectionServiceComponent
  },
  data(){
    return{
     store
    }
  },
  methods:{

  }
}
</script>

<template>

<HeaderComponent />

<MainComponent />

<MainSectionServiceComponent />

<FooterComponent />

<ButtonComponent />


</template>

<style lang="scss">
@use "assets/scss/main" as*;
</style>
