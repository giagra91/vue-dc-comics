<template>
    <div class="products-card">
        <img :src="gameElement.thumb" :alt="gameElement.series">
        <p>{{ gameElement.series }}</p>
        
    </div>
</template>

<script>
export default {
    name: `ProductCard`,
    props: [`gameElement`],

}
</script>

<style lang="scss" scoped>

@import "../assets/scss/partials/variables.scss";

    div.products-card{
    width: calc( 100% / 6);
    height: 25vh;
    padding: 1rem .7rem ;

        img{
            width: 10vw;
            height: 10vw;
            object-fit: cover;
            object-position: top;
            padding-bottom: .4rem;
        }

        p{
            font-size: .8rem;
            font-weight: bold;
            text-transform: uppercase;
        }
        }

</style>