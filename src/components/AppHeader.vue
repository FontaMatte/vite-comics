<script>


export default {

  name: 'AppHeader',
  data() {
    return {

      menuItems: [
                  {
                    title: 'characters',
                    url: '#',
                    active: true
                  },
                  {
                    title: 'comics',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'movies',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'tv',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'games',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'collectibles',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'videos',
                    url: '#',
                    active: false
                  },
                  {
                    title: 'fans',
                    url: '#',
                    active: false
                  },
                  {
                    title: 'news',
                    url: '#',
                    active: false
                  },  
                  {
                    title: 'shop',
                    url: '#',
                    active: false
                  } 
                ]

    };
  },
  components: {

  }
}
</script>

<template>
  <header>

    <div class="container">
      <div class="logo">
        <img src="../assets/img/dc-logo.png" alt="DC-logo">
      </div>
      <div class="nav-bar">
        <ul>
          <li v-for="item in menuItems">
            <a :href="item.url" :class="{active: item.active == true}">
              {{ item.title }}
            </a>
          </li>
        </ul>
      </div>
    </div>

    <div class="jumbotron"></div>

  </header>
</template>

<style lang="scss" scoped>
@import "../styles/partials/appHeader.scss";
</style>