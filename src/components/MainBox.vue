<template>
    <div>
      <!-- 6 JUMBO FRONT CARD -->
      <div class="jumbotron d-flex just-center">
        <div class="row flex-wrap">
          <div class="card" v-for="(post,i) in posts" :key="i" :class="i < 6 ? '' : 'empty'">
            <jumbotron-card v-if="i < 6" :post="post"/>
          </div>
        </div>
      </div>
      <!-- BOTTOM JUMBO SECTION -->
      <div class="content-preview d-flex just-center">
        <div class="row">
          <!-- POPULAR POSTS -->
          <div class="jumbo-column">
            <h2>POPULAR POSTS</h2>
            <div class="card-small" v-for="(postSmall,i) in posts" :key="i" :class="i > 5 && i < 11 ? '' : 'empty'">
              <small-card v-if="i > 5 && i < 11" :postSmall="postSmall"/>
            </div>
          </div>
          <!-- RECENT POSTS -->
          <div class="jumbo-column">
            <h2>RECENT POSTS</h2>
              <div class="card-small" v-for="(postSmall,i) in posts" :key="i" :class="i > 10 && i < 16 ? '' : 'empty'">
              <small-card v-if="i > 10 && i < 16" :postSmall="postSmall"/>
            </div>
          </div>
          <!-- FEATURED POST -->
          <div class="jumbo-column">
            <featured-card :posts="posts"/>
          
          </div>
        </div>
      </div>
      <!-- CATEGORY SLIDER -->
      <div class="category d-flex just-center">
        <div class="row space-between align-center">
          <div><i class="fas fa-angle-left"></i></div>
          <button>GADGETS</button>
          <button>PHOTOGRAPHY</button>
          <button>LIFESTYLE</button>
          <button>FASHION</button>
          <button>RECIPES</button>
          <button>TRAVEL</button>
          <div><i class="fas fa-angle-right"></i></div>
        </div>
      </div>
      <div class="central-page d-flex just-center">
        <div class="row">
          <!-- MAIN POSTS -->
          <div class="main-content">
            <post-card :posts="posts"/>
          </div>
      <!-- SOCIAL MEDIA RECENT POSTS -->
          <div class="latest-socials">
            <!-- TWITTER -->
            <h2>LATEST FROM TWITTER</h2>
            <!-- COMMENT 1 -->
            <div class="twitter-comment d-flex just-center">
              <i class="fab fa-twitter"></i>
              <div>
                <p class="mb-1">If you have any suggestion for the next update, let us know.</p>
                <span>01:05 PM Sep 18th</span>
              </div>
            </div>
            <!-- COMMENT 2 -->
            <div class="twitter-comment d-flex just-center">
              <i class="fab fa-twitter"></i>
              <div>
                <p class="mb-1">We have just updated Porto Admin. Check the changelog for more information.</p>
                <span>01:04 PM Sep 18th</span>
              </div>
            </div>
            <!-- INSTAGRAM -->
            <h2>PHOTOS FROM INSTAGRAM</h2>
            <div class="instagram-post d-flex flex-wrap">
              <img src="/images/29739607_2020680068220520_4509928046932787200_n.jpg" alt="">
              <img src="/images/30087804_253872848488989_8792603541668626432_n.jpg" alt="">
              <img src="/images/29415620_196477127626244_3250318472361541632_n.jpg" alt="">
              <img src="/images/30078414_1274410412703843_8290935809419247616_n.jpg" alt="">
              <img src="/images/30077195_2066750973610181_3733150062893596672_n.jpg" alt="">
              <img src="/images/29415304_166583630713703_1032667922171953152_n.jpg" alt="">
            </div>
            <!-- TAGS -->
            <h2>TAGS</h2>
            <ul class="tags d-flex space-between">
              <li>DESIGN</li>
              <li>BRANDS</li>
              <li>VIDEO</li>
              <li>BUSINESS</li>
              <li>TRAVEL</li>
            </ul>
            <!-- FACEBOOK -->
            <h2>FIND US ON FACEBOOK</h2>
            <span class="facebook-link">
              <a href="#">Okler Themes</a>
            </span>
          </div>
        </div>
      </div>
    </div>
</template>

<script>
import JumbotronCard from './JumbotronCard.vue'
import SmallCard from './SmallCard.vue'
import FeaturedCard from './FeaturedCard.vue'
import PostCard from './PostCard.vue'

export default {
  components: { 
    JumbotronCard,
    SmallCard,
    FeaturedCard,
    PostCard
    },
    props: {
      posts: Array,
    }
    
}
</script>

<style lang="scss">
@import '@/style/variables.scss';
@import '@/style/mainBox.scss';
</style>