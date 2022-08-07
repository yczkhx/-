<template>
  <div>
    <p @click="visible = !visible">Practice2</p>
    <div class="content">
    <RectItem v-if="visible"></RectItem>
    </div>

  </div>
</template>

<script>
// import CilcleItem from '@/components/CircleItem.vue';
import RectItem from '@/components/RectItem.vue';
export default {
  components: { RectItem,},
  data() {
    return {
      visible: true,
    }
  }
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