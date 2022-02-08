<template>
    <div class="card-row">
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
.card-row{
    display: flex;
    align-items: center;
    padding: 15px 0px;
    border-bottom: 2px solid #eee;
    .image-small{
        width: 70px;
        margin-right: 15px;
    }
    .title{
        font-size: 18px;
        color: #333;
    }
    .date{
        font-size: 13px;
        color: #888;
        margin-top: 5px;
    }
}
</style>