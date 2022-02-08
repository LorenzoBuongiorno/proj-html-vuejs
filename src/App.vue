<template>
  <div id="app">
    <header>
      <header-box/>
    </header>
    <main>
      <div class="jumbotron"></div>
      <div class="content-preview">
        <div class="popular-posts"></div>
        <div class="recent-posts"></div>
        <div class="featured-posts"></div>
      </div>
      <div class="category"></div>
      <div class="latest-socials"></div>
      <div class="main-content"></div>
    </main>
    <footer>
      <div class="lable"></div>
      <div class="footer-content"></div>
      <div class="footer-bottom-bar"></div>
    </footer>
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'

export default {
  name: 'App',
  components: {
    HeaderBox

  }
}
</script>

<style lang="scss">
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;900&display=swap');
@import 'style/main.scss';
#app {

}
</style>
