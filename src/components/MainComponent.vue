<script>

import { store } from '../store.js';

export default{
    name: "MainComponent",
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

    <main>
        MAIN
    </main>

</template>

<style lang="scss" scoped>

main{
    padding:40px;
    text-align: center;
}

</style>