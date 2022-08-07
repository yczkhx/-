<template>
  <div>
    Practice2
    <div class="content">
    <RectItem></RectItem>
    </div>

  </div>
</template>

<script>
// import CilcleItem from '@/components/CircleItem.vue';
import RectItem from '@/components/RectItem.vue';
export default {
  components: { RectItem,},
}
</script>

<style scoped>
.content {
  display: flex;
  justify-content: space-around;
}

div {
  font-size: 32px;
}
</style>