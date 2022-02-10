<template>
    <div>
        <div class="post d-flex just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[17].bg_image + '.jpg'" alt="">
                </div>
                <div class="description d-flex">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2 class="mb-2">{{posts[17].title}}</h2>
                        <p class="text">{{posts[17].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="space-between d-flex">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[17].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[17].category" :key="i">
                                    <span v-if="i + 1 == posts[17].category.length">{{genre}}</span>
                                    <span v-else>{{genre + ', '}}</span>
                                    </a>
                                    </span>
                                <span><i class="far fa-comments"></i><a href="#">12 Comments</a></span>
                            </div>
                            <button>READ MORE</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="post d-flex just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[6].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description d-flex">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2 class="mb-2">{{posts[6].title}}</h2>
                        <p class="text">{{posts[6].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="space-between d-flex">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[6].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[6].category" :key="i">
                                    <span v-if="i + 1 == posts[6].category.length">{{genre}}</span>
                                    <span v-else>{{genre + ', '}}</span>
                                    </a>
                                    </span>
                                <span><i class="far fa-comments"></i><a href="#">12 Comments</a></span>
                            </div>
                            <button>READ MORE</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="post d-flex just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[7].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description d-flex">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2 class="mb-2">{{posts[7].title}}</h2>
                        <p class="text">{{posts[7].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="space-between d-flex">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[7].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[7].category" :key="i">
                                    <span v-if="i + 1 == posts[7].category.length">{{genre}}</span>
                                    <span v-else>{{genre + ', '}}</span>
                                    </a>
                                    </span>
                                <span><i class="far fa-comments"></i><a href="#">12 Comments</a></span>
                            </div>
                            <button>READ MORE</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="post d-flex just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[9].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description d-flex">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2 class="mb-2">{{posts[17].title}}</h2>
                        <p class="text">{{posts[9].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="space-between d-flex">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[9].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[9].category" :key="i">
                                    <span v-if="i + 1 == posts[9].category.length">{{genre}}</span>
                                    <span v-else>{{genre + ', '}}</span>
                                    </a>
                                    </span>
                                <span><i class="far fa-comments"></i><a href="#">12 Comments</a></span>
                            </div>
                            <button>READ MORE</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>

        <div class="post d-flex just-center">
            <div>
                <div class="main-image-array d-flex flex-wrap">
                    <img v-for="(img,i) in posts[16].bg_image" :key="i" :src="'/images/blog-' + img + '.jpg'" alt="">
                </div>
                <div class="description d-flex">
                    <div class="date">
                        <div class="date-number">8</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2 class="mb-2">{{posts[16].title}}</h2>
                        <p class="text">{{posts[16].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="space-between d-flex">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[16].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[16].category" :key="i">
                                    <span v-if="i + 1 == posts[16].category.length">{{genre}}</span>
                                    <span v-else>{{genre + ', '}}</span>
                                    </a>
                                    </span>
                                <span><i class="far fa-comments"></i><a href="#">12 Comments</a></span>
                            </div>
                            <button>READ MORE</button>
                        </div>
                    </div>
                </div>
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
.post{
    padding: 20px;
    border-bottom: 2px solid #eee;
    .main-image{
        margin: 20px 0px;
    }
    .description{
       .date{
           text-align: center;
           width: 50px;
           .date-number{
               background-color: #00000008;
               padding: 15px 0px;
               font-weight: 900;
           }
           .date-month{
               background-color: #1c2023;
               color: $light-color;
               text-transform: uppercase;
               font-weight: 900;
               font-size: $default-small-font-size;
           }
       }
       .info{
           width: calc(100% - 50px);
           padding: 0px 20px;
           line-height: 25px;
           h2{
               color: $dark-grey-color;
           }
           .text{
               height: 70px;
               color: $grey-color;
                overflow: hidden;
                text-overflow: ellipsis;
                font-size: $default-font-size;
           }
           .dots{
                color: $grey-color;
                font-size: $default-font-size;
           }
            i{
                color: $grey-color;
                margin-right: 10px;
            }
            a{
                color: $main-blue-color;
                margin-right: 5px;
            }
            button{
                background-color: $light-color;
                border: 2px solid $grey-color;
                padding: 7px;
                border-radius: 8px;
                color: $grey-color;
                cursor: pointer;
            }
       }
    }
    .main-image-array{
        margin: 20px 0px;
        img{
            width: calc(100% / 3);
        }
    }
}

</style>