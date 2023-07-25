<script>

import { store } from '../store.js';

export default{
    name: "MainSectionServiceComponent",
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
    <section class="p-3">
        <div>
            
        </div>
    </section>
</template>

<style lang="scss" scoped>

@use "../assets/scss/partials/mixins" as *;
@use "../assets/scss/main.scss" as *;
@use "../assets/scss/partials/variables.scss" as*;

section{
    background-color: $first-color-bg;
    height: 600px;
    background-image: url(../assets/img/pattern_background.png);
    background-repeat: no-repeat;
    background-position: center;    

}

</style>