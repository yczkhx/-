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
    beforeCreate() {
    console.log('Square: beforeCreate');
  },
  created() {
    console.log('Square: created');

  },
  beforeMount() {
    console.log('Square: beforeMount');

  },
  mounted() {
    console.log('Square: mounted');

  },
  beforeUpdate() {
    console.log('Square: beforeUpdate');

  },
  updated() {
    console.log('Square: updated');

  },
  beforeDestroy() {
    console.log('Square: beforeDestroy');

  },
  destroyed() {
    console.log('Square: destroyed');

  },
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
