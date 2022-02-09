<template>
    <div>
        <div class="post flex-just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[17].bg_image + '.jpg'" alt="">
                </div>
                <div class="description">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2>{{posts[17].title}}</h2>
                        <p class="text">{{posts[17].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="post-data">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[17].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[17].category" :key="i">
                                    <span v-if="i > 0">{{genre}}</span>
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

        <div class="post flex-just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[6].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2>{{posts[6].title}}</h2>
                        <p class="text">{{posts[6].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="post-data">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[6].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[6].category" :key="i">
                                    <span v-if="i > 0">{{genre}}</span>
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

        <div class="post flex-just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[7].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2>{{posts[7].title}}</h2>
                        <p class="text">{{posts[7].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="post-data">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[7].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[7].category" :key="i">
                                    <span v-if="i > 0">{{genre}}</span>
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

        <div class="post flex-just-center">
            <div>
                <div class="main-image">
                    <img class="w-100" :src="'/images/blog-' + posts[9].bg_image + ' (1).jpg'" alt="">
                </div>
                <div class="description">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2>{{posts[17].title}}</h2>
                        <p class="text">{{posts[9].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="post-data">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[9].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[9].category" :key="i">
                                    <span v-if="i > 0">{{genre}}</span>
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

        <div class="post flex-just-center">
            <div>
                <div class="main-image-array">
                    <div class="image-array" v-for="(img,i) in posts[16].bg_image" :key="i">
                        <img class="w-100" :src="'/images/blog-' + img + '.jpg'" alt="">
                    </div>
                </div>
                <div class="description">
                    <div class="date">
                        <div class="date-number">12</div>
                        <div class="date-month">jan</div>
                    </div>
                    <div class="info">
                        <h2>{{posts[16].title}}</h2>
                        <p class="text">{{posts[16].content}}</p>
                        <span class="dots">[...]</span>
                        <div class="post-data">
                            <div>
                                <span><i class="far fa-user"></i><a href="#">{{posts[16].author}}</a></span>
                                <span>
                                    <i class="far fa-folder"></i>
                                    <a href="#" v-for="(genre,i) in posts[16].category" :key="i">
                                    <span v-if="i > 0">{{genre}}</span>
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
       display: flex;
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
               font-size: 15px;
           }
       }
       .info{
           width: calc(100% - 50px);
           padding: 0px 20px;
           line-height: 25px;
           .post-data{
               display: flex;
               justify-content: space-between;
           }
           h2{
               margin-bottom: 20px;
               color: #333;
           }
           .text{
               height: 70px;
               color: #888;
                overflow: hidden;
                text-overflow: ellipsis;
           }
           .dots{
                    color: #888;
           }
            i{
                color: #888;
                margin-right: 10px;
            }
            a{
                color: $main-blue-color;
                margin-right: 5px;
            }
            button{
                background-color: #fff;
                border: 2px solid #888;
                padding: 7px;
                border-radius: 8px;
                color: #888;
                cursor: pointer;
            }
       }
    }
    .main-image-array{
        display: flex;
        flex-wrap: wrap;
        margin-bottom: 20px;
        .image-array{
            width: calc(100% / 3);
            img{
                height: 100%;
            }
        }
    }
}

</style>