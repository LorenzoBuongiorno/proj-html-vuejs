<template>
    <div>
        <img class="w-100" :src="'/images/blog-' + post.bg_image + '.jpg'" alt="">
        <div class="post-introduction">
            <span class="category">{{post.category[0]}}</span>
            <div class="description">{{post.title}}</div>
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
.post-introduction{
    position: absolute;
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
    .description{
        color: $light-color;
        font-weight: 900;
        font-size: 25px;
        margin-top: 20px;
    }
}
</style>