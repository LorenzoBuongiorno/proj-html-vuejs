<template>
    <div>
        <div class="fixed-bar">
            <span>Everything about Lifestyle, Travel and Gadgets!</span>
            <a href="#">SIGN IN</a>
            <a href="#">ABOUT US</a>
            <a href="#">CONTACT US</a>
            <a href="#">BUY NOW</a>
        </div>
        <div class="logo"></div>
        <div class="navbar"></div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.fixed-bar{
    width: 100%;
    position: fixed;
    height: 60px;
    background-color: $main-blue-color;
    display: flex;
    align-items: center;
    font-weight: 900;
    span{
        color: #fff;
        font-size: 14px;
        margin: 0px 15px;
        font-weight: 300;
    }
    a{
        margin: 0px 15px;
    }
}
</style>