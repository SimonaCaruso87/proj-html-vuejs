<script>

import HeaderComponent from './components/HeaderComponent.vue';
import MainComponent from './components/MainComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import ButtonComponent from './components/ButtonComponent.vue';
import ButtonComponentWhite from './components/ButtonComponentWhite.vue';
import SectionServiceComponent from './components/SectionServiceComponent.vue';
import SectionOurWorkComponent from './components/SectionOurWorkComponent.vue';
import SectionOurPlanComponent from './components/SectionOurPlanComponent.vue';
import SectionOurNewsComponent from './components/SectionOurNewsComponent.vue';
import SectionConsultation from './components/SectionConsultation.vue';
import axios from 'axios';
import { store } from './store.js';


export default{
  name:"App",
  components:{
     HeaderComponent ,
     MainComponent ,
     FooterComponent ,
     ButtonComponent ,
     ButtonComponentWhite ,
     SectionServiceComponent ,
     SectionOurWorkComponent ,
     SectionOurPlanComponent ,
     SectionOurNewsComponent ,
     SectionConsultation ,
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

<SectionServiceComponent />

<SectionOurWorkComponent />

<SectionOurPlanComponent />

<SectionOurNewsComponent />

<SectionConsultation />

<FooterComponent />



</template>

<style lang="scss">
@use "assets/scss/main" as*;
</style>
