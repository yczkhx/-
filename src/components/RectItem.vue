<template>
  <div class="rect">
    <p  @click="visible = !visible">Rect</p>
    <button @click="count++">
      RectCount1 {{ count }}
    </button>
    <p>RectCount2 {{rectCount}}</p>
    <div class="children">
      <SquareItem v-if="visible"></SquareItem>
      <CircleItem v-if="visible" :rectCount.sync="rectCount"></CircleItem>
    </div>
  </div>
</template>

<script>
import CircleItem from "./CircleItem.vue";
import { graph, graphCN } from "./dic";
export default {
  components: {
    SquareItem: () => import("./SquareItem.vue"),
    CircleItem,
  },
  data() {
    return {
      count: 0,
      rectCount: 0,
      graph,
      graphCN,
      visible: true,
    };
  },
  beforeCreate() {
    console.log(
      "%c%s %c%s: %cbeforeCreate",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: green"
    );
  },
  created() {
    console.log(
      "%c%s %c%s: %ccreated",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: green"
    );
  },
  beforeMount() {
    console.log(
      "%c%s %c%s: %cbeforeMount",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: brown"
    );
  },
  mounted() {
    console.log(
      "%c%s %c%s: %cmounted",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: brown"
    );
  },
  beforeUpdate() {
    console.log(
      "%c%s %c%s: %cbeforeUpdate",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: green"
    );
  },
  updated() {
    console.log(
      "%c%s %c%s: %cupdated",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: green"
    );
  },
  beforeDestroy() {
    console.log(
      "%c%s %c%s: %cbeforeDestroy",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: red"
    );
  },
  destroyed() {
    console.log(
      "%c%s %c%s: %cdestroyed",
      "color: coral",
      graph[0],
      "color: black",
      graphCN[0],
      "color: red"
    );
  },
};
</script>

<style scoped>
.rect {
  width: 800px;
  height: 600px;
  background-color: coral;
}
.children {
  padding: 10px;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
</style>
