<template>
    <div class="main-footer">
        <div class="label flex-just-center">
            <div class="row">
                <span class="angle"></span>
                <span class="get-in-touch">Get in Touch</span>
            </div>
        </div>
            <div class="footer-content flex-just-center">
                <div class="row">
                    <div class="footer-box">
                        <h2>ABOUT THE BLOG</h2>
                        <p class="about-blog">{{blogInfo.content}}</p>
                        <a :href="blogInfo.url">VIEW MORE ></a>
                    </div>
                    <div class="footer-box">
                        <h2>RECENT POSTS</h2>
                        <ul class="recent">
                           <li v-for="(recentpost,i) in recentPosts" :key="i" :class="i < 2 ? '' : 'empty'">
                               <div v-if="i < 2" class="recent-card">
                                    <img :src="'images/' + recentpost.post_image" alt="">
                                    <div>
                                        <p>{{recentpost.title}}</p>
                                        <span class="date">{{recentpost.date}}</span>
                                    </div>
                               </div>
                            </li> 
                        </ul>
                    </div>
                    <div class="footer-box">
                        <h2>RECENT COMMENTS</h2>
                        <ul class="recent">
                           <li v-for="(recentcomment,i) in recentComments" :key="i" :class="i < 2 ? '' : 'empty'">
                               <div v-if="i < 2">
                                    <div class="recent-comments">
                                        <span class="author">
                                            {{recentcomment.author}}
                                        </span>
                                        <span> commented on </span>
                                        <a :href="recentcomment.url" class="comment-title">
                                        {{recentcomment.post_title_comment}}
                                        </a>
                                    </div>
                                    <span class="date">{{recentcomment.date}}</span>
                               </div>
                            </li> 
                        </ul>
                    </div>
                </div>
            </div>
            <div class="footer-bottom-bar"></div>
    </div>
</template>

<script>
export default {
    props: {
        blogInfo: Object,
        recentPosts: Array,
        recentComments: Array,
         categories: Array
    }
}
</script>

<style lang="scss">
@import '@/style/variables.scss';

    
    .label{
        margin-top: 50px;
          background-color: #212529;
          background: linear-gradient(0deg,  rgba(33,37,41,1) 50%, rgba(255,255,255,1) 50%);
          width: 100%;
          .angle{
              width: 0; 
              height: 0; 
              border-left: 15px solid transparent;
              border-right: 0px solid transparent;
              border-bottom: 37px solid #0074ad;
          }
        .get-in-touch{
            font-family: 'Shadows Into Light', cursive;
            color: #fff;
            font-size: 33px;
            padding: 10px 20px;
            background-color: $main-blue-color;
            display: inline-block;
        }
    }
    .footer-content{
        padding: 30px 0px;
        background-color: #212529;
        .footer-box{
            width: calc(100% / 4 - 30px);
            margin: 0px 15px;
        }
        .about-blog{
            height: 150px;
            line-height: 30px;
            overflow: hidden;
            text-overflow: ellipsis;
            color: #888;
            margin-bottom: 20px ;
        }
        h2{
               margin: 20px 0px;
               color: $light-color;
        }
        a{
          color: $light-color;
          font-weight: 900;
        }
        .recent{
            li{
                margin: 20px 0px;
                .recent-card{
                    display: flex;
                    img{
                        border-radius: 50%;
                        margin-right: 20px;
                    }
                    p{
                        font-size: 18px;
                        font-weight: 900;
                        color: #fff;
                        margin-bottom: 10px;
                    }
                }
                .date{
                    color: #888;
                }
            }
            .recent-comments{
                margin-bottom: 10px;
                span{
                    color: #fff;
                    font-size: 17px;
                    line-height: 30px;
                    
                }
                .author{
                    font-weight: 900;
                }
                .comment-title{
                    color: $main-blue-color;
                }
            }

        }
    }

</style>