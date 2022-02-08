<template>
    <div>
        <div class="fixed-bar flex-just-center">
            <div class="row">
                <span>Everything about Lifestyle, Travel and Gadgets!</span>
                <a href="#">SIGN IN</a>
                <a href="#">ABOUT US</a>
                <a href="#">CONTACT US</a>
                <a href="#">BUY NOW</a>
            </div>
        </div>
        <div class="logo flex-just-center">
            <div class="row">
                <a href="#">
                    <img src="@/assets/images/logo-default-slim.png" alt="">
                </a>
            </div>
        </div>
        <div class="navbar flex-just-center">
            <div class="row">
                <div>
                    <a href="#">HOME</a>
                    <a href="#">ELEMENTS</a>
                    <a href="#">FEATURES</a>
                    <a href="#">PAGES</a>
                    <a href="#">PORTFOLIO</a>
                    <a href="#">BLOG</a>
                    <a href="#">SHOP</a>
                </div>
                <button><i class="fas fa-search"></i></button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.row{
    width: 1700px;
    display: flex;
    align-items: center;
}
.flex-just-center{
    display: flex;
    justify-content: center;
}
.fixed-bar{
    width: 100%;
    height: 60px;
    background-color: $main-blue-color;
    font-weight: 900;
    span{
        font-size: 14px;
        margin: 0px 15px;
        font-weight: 300;
        color: $light-color;
    }
    a{
        color: $light-color;
        margin: 0px 15px;
    }
}
.logo{
    a{
        width: 180px;
        padding: 30px 5px;
        img{
            width: 100%;
        }
    }
}
.navbar{
    padding: 20px 0px;
    border-top: 2px solid #eee;
    a{
        color: #333;
        margin-right: 30px;
        font-weight: 900;
        &:hover{
            color: $main-blue-color;
        }
    }
    button{
        border: 0px;
        background-color: #fff;
        font-size: 18px;
        cursor: pointer;
    }
    .row{
        justify-content: space-between;
    }
}
</style>