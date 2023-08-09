<script>
export default{
    props:{
        currentCard:{
            type: Object,
            default: {}
        }
    },
    methods:{
        getImgPath: (imgSrc)=> {
            return new URL(imgSrc, import.meta.url).href;
        },
    }
}
</script>

<template>
    <div class="card">
        <div class="hover-link">
            <a href="">
                <font-awesome-icon icon="fa-solid fa-link" />
            </a>
        </div>
        <img class="normal" :src="getImgPath(currentCard.linkImg)" alt="">
    </div>
</template>

<style lang="scss" scoped>
    .card{
        width: calc((100% - 20px ) / 3);
        height: 300px;
        cursor: pointer;
        position: relative;
        img{
            min-width: 100%;
            min-height: 100%;
            object-fit: cover;
        }

        .hover-link{
            position: absolute;
            width: 100%;
            height: 100%;
            transition: opacity 200ms ease-in-out,
                        visibility 200ms ease-in-out;
            background: linear-gradient(180deg, rgba(4,84,161,1) 18%, rgba(255,255,255,1) 86%);
            opacity: 0;
            visibility: hidden;
            a{
                width: 100%;
                height: 100%;
                display: flex;
                align-items: center;
                justify-content: center;
                font-size: 35px;
                color: #f5f5f5;;
            }
        }
        &:hover .hover-link{
            opacity: 1;
            visibility: visible;
        }
    }
</style>