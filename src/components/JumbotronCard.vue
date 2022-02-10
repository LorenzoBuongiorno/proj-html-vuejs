<template>
    <div>
        <!-- MAIN JUMBO CARD -->
        <a class="cover" :href="post.url"></a>
        <div class="dark-layer"></div>
        <img class="w-100" :src="'/images/blog-' + post.bg_image + '.jpg'" alt="">
        <div class="post-introduction">
            <span class="category">{{post.category[0]}}</span>
            <div class="title">{{post.title}}</div>
            <div class="description">{{post.description}}</div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        post: Object
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.cover{
    position: absolute;
    z-index: 4;
    width: 100%;
    height: 100%;
    cursor: pointer;
    &:hover ~ .dark-layer{
        opacity: 60%;
        transition: opacity 0.3s;
    }
    &:hover ~ .post-introduction .description{
        display: block;
    }
}
.dark-layer{
    background-color: #000;
    width: 100%;
    height: 100%;
    opacity: 0%;
    position: absolute;
    z-index: 2;
    transition: opacity 0.3s;
}
.post-introduction{
    position: absolute;
    z-index: 3;
    bottom: 0px;
    padding: 20px;
    .category{
        color: $light-color;
        text-transform: uppercase;
        font-weight: 900;
        padding: 10px;
        font-size: $default-small-font-size;
        background-color: $main-blue-color;
    }
    .title{
        color: $light-color;
        font-weight: 900;
        font-size: $default-title-font-size;
        margin-top: 20px;
    }
    .description{
        margin-top: 10px;
        font-size: $default-font-size;
        line-height: 30px;
        color: $grey-color;
        font-weight: 900;
        display: none;
    }
}
</style>