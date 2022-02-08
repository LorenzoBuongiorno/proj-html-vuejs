<template>
    <div>
      <div class="jumbotron flex-just-center">
        <div class="row">
          <div class="card" v-for="(post,i) in posts" :key="i" :class="i < 6 ? '' : 'empty'">
            <jumbotron-card v-if="i < 6" :post="post"/>
          </div>
        </div>
      </div>
      <div class="content-preview">
        <div class="popular-posts"></div>
        <div class="recent-posts"></div>
        <div class="featured-posts"></div>
      </div>
      <div class="category"></div>
      <div class="latest-socials"></div>
      <div class="main-content"></div>
    </div>
</template>

<script>
import JumbotronCard from './JumbotronCard.vue'

export default {
  components: { 
    JumbotronCard,

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
</style>