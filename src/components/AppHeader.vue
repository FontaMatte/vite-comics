<script>

export default {

  name: 'AppHeader',
  data() {
    return {

      menuItems: ['characters','comics','movies',
                  'tv','games','collectibles','videos',
                  'fans','news','shop']

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
            <a href="#">{{ item }}</a>
          </li>
        </ul>
      </div>
    </div>

  </header>
</template>

<style lang="scss" scoped>
@import "../styles/partials/appHeader.scss";
</style>