<template>
    <div>
        <div class="cover"></div>
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
        display: block;
    }
    &:hover ~ .post-introduction .description{
        display: block;
    }
}
.dark-layer{
    background-color: #000;
    width: 100%;
    height: 100%;
    opacity: 60%;
    position: absolute;
    z-index: 2;
    display: none;
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
        font-size: 15px;
        background-color: $main-blue-color;
    }
    .title{
        color: $light-color;
        font-weight: 900;
        font-size: 25px;
        margin-top: 20px;
    }
    .description{
        margin-top: 10px;
        font-size: 20px;
        line-height: 30px;
        color: #888;
        font-weight: 900;
        display: none;
    }
}
</style>