<template>
    <div>
      <div class="jumbotron">
        <div v-for="(post,i) in posts" :key="i">
          <jumbotron-card v-if="i < 6" :post="post"/>
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

</style>