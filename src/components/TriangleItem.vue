<template>
  <div class="triangle">
    <p>Triangle</p>
  </div>
</template>
<script>
export default {
  beforeCreate() {
    console.log('Triangle: beforeCreate');
  },
  created() {
    console.log('Triangle: created');

  },
  beforeMount() {
    console.log('Triangle: beforeMount');

  },
  mounted() {
    console.log('Triangle: mounted');

  },
  beforeUpdate() {
    console.log('Triangle: beforeUpdate');

  },
  updated() {
    console.log('Triangle: updated');

  },
  beforeDestroy() {
    console.log('Triangle: beforeDestroy');

  },
  destroyed() {
    console.log('Triangle: destroyed');

  },
}
</script>
<style scoped>
.triangle {
  width: 0;
  height: 0;
  border-left: 100px solid transparent;
  border-right: 100px solid transparent;
  border-bottom: 200px solid chocolate;
}

p {
  position: relative;
  left: -54px;
  bottom: -80px;
}
</style>