<template>
    <div>
        <h2>FEATURED POSTS</h2>
        <div class="featured-card-post">
            <div class="dark-layer"></div>
            <img class="w-100" :src="'/images/blog-' + posts[12].bg_image + ' (1).jpg'" alt="">
            <div class="post-introduction">
                <span class="category">{{posts[12].category[0]}}</span>
                <div class="title">{{posts[12].title}}</div>
            </div>
        </div>
        <h2>FEATURED AUTHOR</h2>
        <div class="featured-card-author d-flex align-center">
            <div class="author-pic">
                <img class="w-100" :src="'/images/avatar.jpg'" alt="">
            </div>
            <div>
                <div class="author mb-1">{{posts[12].author}}</div>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Explicabo, consequatur ipsa adipisci possimus vitae eveniet id commodi, laudantium excepturi unde eligendi ipsum?</p>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props: {
        posts: Array
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.featured-card-post{
    position: relative;
    .dark-layer{
        position: absolute;
        width: 100%;
        height: 100%;
        background-color: rgba($color: #000000, $alpha: 0.5);
    }
    .post-introduction{
        position: absolute;
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
        }
    }
}
.featured-card-author{
    .author-pic{
        width: 900px;
        padding: 20px;
    }
    .author{
        font-weight: 900;
        font-size: $default-font-size;
        color: $dark-grey-color;
    }
    p{
        color: $grey-color;
    }
}
</style>