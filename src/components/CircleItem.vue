<template>
  <div class="circle">
    <p>Circle</p>
    <button @click="count++">
      {{ count }}
    </button>
    <p>computed: {{ countListen }}</p>
    <p>watch {{ countWatcher }}</p>
  </div>
</template>

<script>
import { graph, graphCN } from "./dic";
export default {
  data() {
    return {
      count: 0,
      graph,
      graphCN,
      countWatcher: 0,
    };
  },
  computed: {
    countListen() {
      console.log(
        "%c%s %c%s: computed",
        "color: aqua",
        graph[3],
        "color: black",
        graphCN[3],
        this.count
      );
      return this.count;
    },
  },
  watch: {
    count() {
      console.log(
        "%c%s %c%s: watch",
        "color: aqua",
        graph[3],
        "color: black",
        graphCN[3],
        this.count
      );
      this.countWatcher = this.count;
    },
  },
  beforeCreate() {
    console.log(
      "%c%s %c%s: %cbeforeCreate",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: green"
    );
  },
  created() {
    console.log(
      "%c%s %c%s: %ccreated",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: green"
    );
  },
  beforeMount() {
    console.log(
      "%c%s %c%s: %cbeforeMount",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: brown"
    );
  },
  mounted() {
    console.log(
      "%c%s %c%s: %cmounted",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: brown"
    );
  },
  beforeUpdate() {
    console.log(
      "%c%s %c%s: %cbeforeUpdate",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: green"
    );
  },
  updated() {
    console.log(
      "%c%s %c%s: %cupdated",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: green"
    );
  },
  beforeDestroy() {
    console.log(
      "%c%s %c%s: %cbeforeDestroy",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: red"
    );
  },
  destroyed() {
    console.log(
      "%c%s %c%s: %cdestroyed",
      "color: aqua",
      graph[3],
      "color: black",
      graphCN[3],
      "color: red"
    );
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
