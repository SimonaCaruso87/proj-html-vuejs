<script>

import { store } from '../store.js';

export default{
    name: "HeaderComponent",
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

    <header>
        HEADER
    </header>

</template>

<style lang="scss" scoped>

header{
    padding:40px;
    text-align: center;
}

</style>