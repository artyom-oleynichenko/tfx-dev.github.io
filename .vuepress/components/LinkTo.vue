<template>
  <router-link :to="'pages/' + link" class="feature">
    <h2>{{ name }}</h2>
    <img :src="`${img}.png`"/>
  </router-link>
</template>

<script>
export default {
  props: ["name", "link", "img"],
}
</script>

<style lang="stylus" scoped>
.feature
  h2, img
    transition all .5s ease

  img
    opacity .7

  &:hover
    img
      opacity 1

    h2
      color #000
</style>