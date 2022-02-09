<template>
  <div id="app">
    <header>
      <header-box :nav="nav"/>
    </header>
    <main>
    <main-box :posts="posts"/>
    </main>
    <footer>
      <footer-box
      :blogInfo="blogInfo"
      :recentPosts="recentPosts"
      :recentComments="recentComments"
      :categories="categories"
      />
    </footer>
  </div>
</template>

<script>
import HeaderBox from './components/HeaderBox.vue'
import MainBox from './components/MainBox.vue'
import FooterBox from './components/FooterBox.vue'

export default {
  name: 'App',
  components: {
    HeaderBox,
    MainBox,
    FooterBox

  },
  data () {
    return {
      nav: [
        {
          section: 'SIGN IN',
          url: '#'
        },
        {
          section: 'ABOUT',
          url: '#'
        },
        {
          section: 'CONTACT US',
          url: '#'
        },
        {
          section: 'BUY NOW',
          url: '#'
        },
        {
          section: 'HOME',
          url: '#'
        },
        {
          section: 'ELEMENTS',
          url: '#'
        },
        {
          section: 'FEATURES',
          url: '#'
        },
        {
          section: 'PAGES',
          url: '#'
        },
        {
          section: 'PORTFOLIO',
          url: '#'
        },
        {
          section: 'BLOG',
          url: '#'
        },
        {
          section: 'SHOP',
          url: '#'
        },
        
      ],
      posts: [
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'How To Take Better Concert Pictures in 30 Seconds',
          category: [
            'photography'
            ],
          bg_image: 46,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Gadgets That Make Your Smartphone Even Smarter',
          category: [
            'gadgets'
            ],
          bg_image: 47,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '20Top-Rated Tourist Attractions in Manhattan',
          category: [
            'travel'
            ],
          bg_image: 48,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'The Best Way to Ride a Motorcycle',
          category: [
            'lifestyle'
            ],
          bg_image: 49,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '5 Fun Things to Do at the Beach',
          category: [
            'travel'
            ],
          bg_image: 50,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Amazingly Fresh Fruit And Herb Drinks For Summer',
          category: [
            'recipes'
            ],
          bg_image: 51,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Simple Ways to Have a Pretty Face',
          category: [
            'photography',
            'travel'
            ],
          bg_image: 55,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Ranking the greatest players in basketball',
          category: [
            'sports',
            'businnes'
            ],
          bg_image: 56,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '4 Ways to Look Cool in Glasses',
          category: [
            'photography'
            ],
          bg_image: 57,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Top Camper Trailer Towing Tips',
          category: [
            'travel',
            'lifestyle'
            ],
          bg_image: 58,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '5 Lovely Walks in New York',
          category: [
            'travel'
            ],
          bg_image: 59,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Main Reasons To Stop Texting And Driving',
          category: [
            'travel'
            ],
          bg_image: 65,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Tips to Help You Quickly Prepare your Lunch',
          category: [
            'recipes'
            ],
          bg_image: 66,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'Why should I buy a smartwatch?',
          category: [
            'gadgets'
            ],
          bg_image: 67,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'The best augmented reality smartglasses',
          category: [
            'gadgets'
            ],
          bg_image: 68,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '12 Healthiest Food to Eat for Breakfast',
          category: [
            'recipes'
            ],
          bg_image: 69,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: '10 Best Travel Tips After 5 year Traveling The World',
          category: [
            'travel',
            'lifestyle'
            ],
          bg_image: [
            13,
            16,
            20,
            23,
            29,
            40
          ],
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
        {
          author: 'John Doe',
          profile_pic: 'avatar',
          title: 'How to Make Friends as a Grown-Up',
          category: [
            'lifestyle',
            'travel'
            ],
          bg_image: 54,
          date: 'January 12, 2019',
          description: 'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et!',
          content:'Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!Harum doloribus laudantium culpa laboriosam amet quis neque eaque esse praesentium et aspernatur distinctio laborum excepturi ut error voluptate reprehenderit, totam dolorem!',
        },
      ],
      blogInfo: 'Lorem ipsum dolor sit, amet consectetur adipisicing elit. Ut, doloribus, laborum labore perferendis mollitia accusantium voluptatem dolorem sint nesciunt esse magnam hic impedit cupiditate. Quae dolorum id repellat dignissimos deleniti. Lorem ipsum, dolor sit amet consectetur adipisicing elit. Porro illo perferendis nisi doloremque magni, ... architecto alias excepturi totam sunt vero quis, odit aperiam possimus veritatis officiis atque repellendus eos quisquam. Lorem ipsum dolor sit amet consectetur adipisicing elit. Similique distinctio suscipit perspiciatis veniam ducimus laudantium, ea dolor vel a officia deleniti, eius rerum laboriosam eligendi possimus porro facilis nulla consequatur?',
      recentPosts: [
        {
          title: 'Lorem ipsum dolor sit, consectetur adipiscing alit.',
          date: '12:53 AM Dec 19th',
          post_image: 'our-office-4-square.jpg'
        },
        {
          title: 'Lorem ipsum dolor sit, consectetur adipiscing alit.',
          date: '12:53 AM Dec 19th',
          post_image: 'our-office-5-square.jpg'
        },
      ],
      recentComments: [
        {
          author: 'John Doe',
          post_title_comment: 'lorem ipson dolor sit amet.',
          date: '12:55 AM Dec 19th'
        },
        {
          author: 'John Doe',
          post_title_comment: 'lorem ipson dolor sit amet.',
          date: '12:55 AM Dec 19th'
        },
        
      ],
      categories: [
        'gadgets',
        'photography',
        'lifestyle',
        'fashion',
        'recipes',
        'travel',
        'business',
        'architecture',
        'reviews',
        'sports',
        'videos',
        'technology',
        'design',

      ]
    }
  }
}
</script>

<style lang="scss">
@import url('https://use.fontawesome.com/releases/v5.7.1/css/all.css');
@import url('https://fonts.googleapis.com/css2?family=Lato:wght@300;400;900&family=Shadows+Into+Light&display=swap');
@import 'style/main.scss';

</style>
