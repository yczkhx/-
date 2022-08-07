<template>
  <div class="circle">
    Circle
    <!-- <TriangleItem></TriangleItem> -->
    <!-- <RectItem></RectItem> -->

  </div>
</template>

<script>
export default {
  beforeCreate() {
    console.log('Circle: beforeCreate');
  },
  created() {
    console.log('Circle: created');

  },
  beforeMount() {
    console.log('Circle: beforeMount');

  },
  mounted() {
    console.log('Circle: mounted');

  },
  beforeUpdate() {
    console.log('Circle: beforeUpdate');

  },
  updated() {
    console.log('Circle: updated');

  },
  beforeDestroy() {
    console.log('Circle: beforeDestroy');

  },
  destroyed() {
    console.log('Circle: destroyed');

  },
};
</script>

<style scoped>
.circle {
  width: 300px;
  height: 300px;
  border-radius: 50%;
  background-color: aqua;
}
</style>