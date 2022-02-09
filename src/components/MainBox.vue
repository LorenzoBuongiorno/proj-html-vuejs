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
      <div class="category flex-just-center">
        <div class="row">
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
      <div class="central-page flex-just-center">
        <div class="row">
          <div class="main-content">
            <post-card :posts="posts"/>
          </div>
          <div class="latest-socials">
            <h2>LATEST FROM TWITTER</h2>
            <!-- COMMENT 1 -->
            <div class="twitter-comment flex-just-center">
              <i class="fab fa-twitter"></i>
              <div>
                <p>If you have any suggestion for the next update, let us know.</p>
                <span>01:05 PM Sep 18th</span>
              </div>
            </div>
            <!-- COMMENT 2 -->
            <div class="twitter-comment flex-just-center">
              <i class="fab fa-twitter"></i>
              <div>
                <p>We have just updated Porto Admin. Check the changelog for more information.</p>
                <span>01:04 PM Sep 18th</span>
              </div>
            </div>
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
.category{
  background-color: $main-blue-color;
  .row{
    justify-content: space-between;
    align-items: center;
    i{
      font-size: 30px;
      color: #333;
    }
    button{
      border: 0px;
      background-color: #404040;
      color: $light-color;
      font-weight: 900;
      font-size: 20px;
      width: calc(100% / 6 - 30px);
      height: 70px;
      margin: 50px 15px;
      cursor: pointer;
    }
  }
  
}
.main-content{
  width: 70%;
}
.latest-socials{
  padding: 30px;
  width: 30%;
  h2{
    color: #333;
  }
  .twitter-comment{
    padding-top: 30px;
    .fa-twitter{
      font-size: 30px;
      color: #333;
    }
    div{
      margin-left: 15px;
      p{
        color: #888;
        margin-bottom: 15px;
        font-size: 18px;
      }
      span{
        color: $main-blue-color;
      }
    }
  }
}



</style>