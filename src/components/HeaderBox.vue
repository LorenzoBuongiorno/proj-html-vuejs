<template>
    <div>
        <div class="fixed-bar d-flex just-center w-100 align-center">
            <div class="row">
                <span>Everything about Lifestyle, Travel and Gadgets!</span>
                <ul class="d-flex just-center">
                    <li v-for="(element,i) in nav" :key="i"><a :href="element.url" :class="i < 4 ? '' : 'empty'">{{element.section}}</a></li>
                </ul>
            </div>
        </div>
        <div class="logo d-flex just-center">
            <div class="row">
                <a href="#">
                    <img src="/images/logo-default-slim.png" alt="">
                </a>
            </div>
        </div>
        <div class="navbar d-flex just-center">
            <div class="row space-between align-center">
                <ul class="d-flex just-center">
                    <li v-for="(element,i) in nav" :key="i"><a :href="element.url" :class="i > 3 ? '' : 'empty'">{{element.section}}</a></li>
                </ul>
                <div>
                    <input type="text" placeholder="search">
                    <button><i class="fas fa-search"></i></button>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    props:{
        nav: Array
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
.fixed-bar{
    height: 60px;
    background-color: $main-blue-color;
    font-weight: 900;
    span{
        font-size: $default-small-font-size;
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
        color: $dark-grey-color;
        margin-right: 30px;
        font-weight: 900;
        &:hover{
            color: $main-blue-color;
        }
    }
    input{
        border: 0px;
        padding: 10px;
        margin-right: 10px;
    }
    button{
        border: 0px;
        background-color: $light-color;
        font-size: $default-font-size;
        cursor: pointer;
    }
}
</style>