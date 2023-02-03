<script>

export default {

  name: 'AppShop',
  data() {
    return {

      shopLinks: [
        {
          img: 'buy-comics-digital-comics.png',
          title: 'DIGITAL COMICS'
        },
        {
          img: 'buy-comics-merchandise.png',
          title: 'DC MERCHANDISE'
        },
        {
          img: 'buy-comics-subscriptions.png',
          title: 'SUBSCRIPTION'
        },
        {
          img: 'buy-comics-shop-locator.png',
          title: 'COMIC SHOP LOCATOR'
        },
        {
          img: 'buy-dc-power-visa.svg',
          title: 'DC POWER VISA'
        },
      ]

    };
  },
  methods: {
    getImagePath: function(imgPath) {
      return new URL(imgPath, import.meta.url).href;
    }
  },
}
</script>

<template>
  <section>
    <div class="container">
        <ul class="shop-menu-items">
          <li v-for="link in shopLinks">
            <a href="#" class="img">
              <img :src="getImagePath(`./../assets/img/${ link.img }`)" alt="">
            </a>
            <a href="#" class="title">
              {{ link.title }}
            </a>
          </li>
        </ul>
    </div>
  </section>
</template>

<style lang="scss" scoped>
@import "../styles/partials/appShop.scss";
</style>