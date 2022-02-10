<template>
    <div class="main-footer">
        <!-- GET IN TOUCH LABEL -->
        <div class="label d-flex just-center">
            <div class="row">
                <span class="angle"></span>
                <span class="get-in-touch">Get in Touch</span>
            </div>
        </div>
            <div class="footer-content d-flex just-center">
                <div class="row">
                    <!-- ABOUT THE BLOG -->
                    <div class="footer-box">
                        <h2>ABOUT THE BLOG</h2>
                        <p class="about-blog mb-2">{{blogInfo.content}}</p>
                        <a :href="blogInfo.url">VIEW MORE ></a>
                    </div>
                    <div class="footer-box">
                        <!-- RECENT POSTS -->
                        <h2>RECENT POSTS</h2>
                        <ul class="recent">
                           <li v-for="(recentpost,i) in recentPosts" :key="i" :class="i < 2 ? '' : 'empty'">
                               <div v-if="i < 2" class="recent-card d-flex">
                                    <img :src="'images/' + recentpost.post_image" alt="">
                                    <div>
                                        <p class="mb-1">{{recentpost.title}}</p>
                                        <span class="date">{{recentpost.date}}</span>
                                    </div>
                               </div>
                            </li> 
                        </ul>
                    </div>
                    <div class="footer-box">
                        <!-- RECENT COMMENTS -->
                        <h2>RECENT COMMENTS</h2>
                        <ul class="recent">
                           <li v-for="(recentcomment,i) in recentComments" :key="i" :class="i < 2 ? '' : 'empty'">
                               <div v-if="i < 2">
                                    <div class="recent-comments mb-1">
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
                    <div class="footer-box">
                        <!-- CATEGORIES -->
                        <h2>CATEGORIES</h2>
                        <ul>
                            <li class="category-tag" v-for="(category,i) in categories" :key="i">
                                {{category}}
                            </li>
                        </ul>
                    </div>
                </div>
            </div>
            <!-- FOOTER BOTTOM BAR -->
            <div class="footer-bottom-bar d-flex just-center">
                <div class="row space-between">
                    <div class="copyright d-flex align-center">
                        <img src="images/logo-footer.png" alt="">
                        <span>&copy; Copyright 2020. All Rights Reserved.</span>
                    </div>
                    <div class="copyright d-flex align-center">
                        <a href="#">> FAQ's</a>
                        <a href="#">> Sitemap</a>
                        <a href="#">> Contact Us</a>
                    </div>
                </div>
            </div>
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
@import '@/style/footerBox.scss';

</style>