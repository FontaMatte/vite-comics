<script>

import AppShop from './AppShop.vue';

export default {

  name: 'AppFooter',
  data() {
    return {

      listItems1 : ['Characters','Comics','Movies','TV','Games','Videos','News'],
      listItems2 : ['Shop DC','Shop DC collectibles'],
      listItems3 : ['Terms Of Use','Privacy Policy (New)','Ad Choices','Advertising','Jobs',
                    'Subscription','Talent Workshop','CPSC Certification','Ratings','Shop Help','Contact Us'],
      listItems4 : ['DC','MAD Magazine','DC Kids','DC Universe','DC Power Visa'],
      socialIcons : ['footer-facebook.png',
                    'footer-periscope.png',
                    'footer-pinterest.png',
                    'footer-twitter.png',
                    'footer-youtube.png']

    };
  },
  methods: {
    getImagePath: function(imgPath) {
      return new URL(imgPath, import.meta.url).href;
    }
  },
  components: {
    AppShop
  }
}
</script>

<template>
  <footer>

      <AppShop/>
    
      <div class="footer-top">
        <div class="container">
          <div class="list1">
            <h3>
              DC COMICS
            </h3>
            <ul>
              <li v-for="item in listItems1">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
            <h3>
              SHOP
            </h3>
            <ul>
              <li v-for="item in listItems2">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>

          <div class="list2">
            <h3>
              DC
            </h3>
            <ul>
              <li v-for="item in listItems3">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>

          <div class="list3">
            <h3>
              SITES
            </h3>
            <ul>
              <li v-for="item in listItems4">
                <a href="#">{{ item }}</a>
              </li>
            </ul>
          </div>
        </div>
      </div>
      <div class="footer-bottom">
        <div class="container">
          <div class="call-to-action">
            <button>
              SIGN-UP NOW!
            </button>
          </div>
          <div class="social">
            <h3>
              <a href="#">FOLLOW US</a> 
            </h3>
            <ul>
              <li v-for="icon in socialIcons">
                <a href="#">
                  <img :src="getImagePath(`./../assets/img/${ icon }`)" alt="">
                </a>
              </li>
            </ul>

          </div>
        </div>
      </div>

  </footer>
</template>

<style lang="scss" scoped>
@import "../styles/partials/appFooter.scss";
</style>