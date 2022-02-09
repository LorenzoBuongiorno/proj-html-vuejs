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
                        <p class="about-blog">{{blogInfo}}</p>
                    </div>
                    <div class="footer-box"></div>
                    <div class="footer-box"></div>
                </div>
            </div>
            <div class="footer-bottom-bar"></div>
    </div>
</template>

<script>
export default {
    props: {
        blogInfo: String,
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
        padding-top: 30px;
        background-color: #212529;
        .footer-box{
            width: calc(100% / 3 - 30px);
            margin: 0px 15px;
        }
        .about-blog{
            height: 150px;
            line-height: 30px;
            overflow: hidden;
            text-overflow: ellipsis;
            color: #888;
        }
        h2{
               margin-bottom: 20px;
               color: $light-color;
           }
    }

</style>