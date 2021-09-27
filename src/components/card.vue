<template>
    <div class="comics-single-card">
        <div class="image-container">
            <img :src="image" :alt="series">
        </div>
        <p>{{series}}</p>
    </div>
</template>

<script>
export default {
    name :"card",
    props : ["image", "price", "series","type"],
}
</script>

<style lang="scss" scoped> 
@import "../style/variables.scss";

    .comics-single-card{
        width: calc(100% / 6 - 40px);
        margin: 10px;
    }

    .image-container {
        height: 170px;
        img {
            height: 100%;
            width: 100%;
            object-fit: cover;
            object-position: top;
        }
    }

    p{
        color: $whiteText ;
    }
</style>