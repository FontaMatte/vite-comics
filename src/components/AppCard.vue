<script>

export default {

  name: 'AppCard',
  props: {
    series: String,
    thumb: String
  },
  data() {
    return {

    };
  },
}
</script>

<template>

        <div>
          <div>
            <img :src="thumb" :alt="series">
          </div>
          <h4>
            {{ series }}
          </h4>
        </div>
        
</template>

<style lang="scss" scoped>

</style>