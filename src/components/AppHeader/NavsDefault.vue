<template>
  <nav class="navs">
    <!-- <router-link
      class="navs__nav"
      to="/search"
    >
      <img
        src="/public/2.0/icons/search-white.png"
        alt=""
      >
    </router-link>
    <router-link
      class="navs__nav"
      to="/following"
    >
      <img
        src="/public/2.0/icons/follow-white-bold.png"
        alt=""
      >
    </router-link> -->
    <NavsDefaultUser
      class="navs__nav"
    />
  </nav>
</template>

<script>
import NavsDefaultUser from './NavsDefaultUser.vue'

export default {
  components: {
    NavsDefaultUser
  }
}
</script>

<style lang="stylus" scoped>
.navs
  display flex
  align-items center
  &__nav
    display flex
    height 24px
    align-items center
    cursor pointer
    & + &
      margin 0 0 0 20px
    img
      height 100%

@media (min-width: 768px)
  .navs
    &__nav
      height 30px
      & + &
        margin 0 0 0 30px
</style>
