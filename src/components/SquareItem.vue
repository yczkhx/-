<template>
  <div class="square">
    Square
    <div class="children">
      <TriangleItem></TriangleItem>
    </div>
  </div>
</template>
<script>
import TriangleItem from "./TriangleItem.vue";
export default {
  components: { TriangleItem },
};
</script>
<style scoped>
.square {
  width: 300px;
  height: 300px;
  background-color: gold;
}
.children {
  display: flex;
  justify-content: space-around;
  align-items: center;
}
</style>
