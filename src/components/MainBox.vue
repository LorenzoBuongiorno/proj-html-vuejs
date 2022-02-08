<template>
    <div>
      <div class="jumbotron flex-just-center">
        <div class="row">
          <div class="card" v-for="(post,i) in posts" :key="i" :class="i < 6 ? '' : 'empty'">
            <jumbotron-card v-if="i < 6" :post="post"/>
          </div>
        </div>
      </div>
      <div class="content-preview flex-just-center">
        <div class="row">
          <div class="jumbo-column popular-posts">
            <h2>POPULAR POSTS</h2>
            <div class="card-small" v-for="(postSmall,i) in posts" :key="i" :class="i > 5 && i < 11 ? '' : 'empty'">
              <small-card v-if="i > 5 && i < 11" :postSmall="postSmall"/>
            </div>
          </div>
          <div class="jumbo-column recent-posts">
            <h2>RECENT POSTS</h2>
              <div class="card-small" v-for="(postSmall,i) in posts" :key="i" :class="i > 10 && i < 16 ? '' : 'empty'">
              <small-card v-if="i > 10 && i < 16" :postSmall="postSmall"/>
            </div>
          </div>
          <div class="jumbo-column featured-posts">
            <featured-card :posts="posts"/>
          
          </div>
        </div>
      </div>
      <div class="category"></div>
      <div class="latest-socials"></div>
      <div class="main-content"></div>
    </div>
</template>

<script>
import JumbotronCard from './JumbotronCard.vue'
import SmallCard from './SmallCard.vue'
import FeaturedCard from './FeaturedCard.vue'

export default {
  components: { 
    JumbotronCard,
    SmallCard,
    FeaturedCard
    },
    props: {
      posts: Array,
    }
    
}
</script>

<style lang="scss">
.jumbotron{
  background-color: #d6d6d6;
  .card{
    width: calc(100% / 3 - 30px);
    margin: 15px;
    position: relative;
  }
  .row{
    margin: 40px 0px;
    flex-wrap: wrap;
  }
}
.content-preview{
  .jumbo-column{
    width: calc(100% / 3 - 20px);
    margin: 0px 10px;
  }
  h2{
    margin: 30px 0px;
    color: #333;
  }
}
</style>