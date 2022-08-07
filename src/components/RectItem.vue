<template>
  <div class="rect">
    Rect
    <div class="children">
      <SquareItem></SquareItem>
      <CircleItem></CircleItem>
    </div>
  </div>
</template>

<script>
import CircleItem from './CircleItem.vue'
export default {
  components: {
    SquareItem: ()=> import('./SquareItem.vue'),
    CircleItem,
  }
}
</script>

<style scoped>
.rect {
  width: 800px;
  height: 600px;
  background-color: coral;
}
.children {
  padding: 30px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>