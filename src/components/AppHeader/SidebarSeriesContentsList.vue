<template>
  <ol class="list">
    <ListItem
      v-for="(item, i) in items"
      :key="i"
      :item="item"
      class="list__list-item"
    />
  </ol>
</template>

<script>
import ListItem from './SidebarSeriesContentsListItem.vue'

export default {
  components: {
    ListItem
  },
  props: {
    items: {
      type: Array,
      default: () => [],
      required: true
    }
  }
}
</script>

<style lang="stylus" scoped>
.list
  list-style none
  margin 0
  padding 0
  &__list-item
    & + &
      margin 17px 0 0 0

@media (min-width: 768px)
  .list
    &__list-item
      & + &
        margin 30px 0 0 0
</style>
