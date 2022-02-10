<template>
    <div class="card-row d-flex">
        <a class="card-cover" :href="postSmall.url"></a>
        <div class="image-small">
            <img class="w-100" :src="'/images/blog-' + postSmall.bg_image + '.jpg'" alt="">
        </div>
        <div>
            <div class="title">{{postSmall.title}}</div>
            <div class="date">{{postSmall.date}}</div>
        </div>
    </div>
</template>

<script>
export default {
    
    props: {
        postSmall: Object
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.card-row{
    align-items: center;
    padding: 15px 0px;
    border-bottom: 2px solid #eee;
    position: relative;
    .card-cover{
        position: absolute;
        z-index: 5;
        width:100% ;
        height: 100%;
        cursor: pointer;
        &:hover ~ .image-small{
            transform: scale(105%);
            transition: transform 0.3s;
        }
        &:hover ~ div .title{
            color: $main-blue-color;
        }
    }
    .image-small{
        width: 70px;
        margin-right: 15px;
        transition: transform 0.3s;
    }
    .title{
        font-size: $default-font-size;
        color: $dark-grey-color;
    }
    .date{
        font-size: 13px;
        color: $grey-color;
        margin-top: 5px;
    }
}
</style>