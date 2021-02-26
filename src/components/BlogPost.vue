<template>
  <div>
    <button v-on:click="$emit('enlarge-text',0.1)">Enlarge Button</button>
    <h1>{{title}}</h1>

  </div>
</template>
<script>
// in props  number;boolean;array;object need to use v-bind:
//  单向数据流
// 1.防止子组件以外变更父级组件的状态
// 2。父组件变更时候 子组件自己刷新成最新 所以不能在子组件中更改prop
export default {
  // props: ["title"],
  props: {
    title: {
      type: String,
      default: "title",
      require: true,
    },
  },
};
</script>
<style scoped>
</style>