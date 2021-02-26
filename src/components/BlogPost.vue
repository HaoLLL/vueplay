<template>
<div>
    <button v-on:click="$emit('enlarge-text',0.1)">Enlarge Button</button>
  <h1>{{title}}</h1>

</div>
</template>
<script>
export default {
  props: ["title"],
 
};
</script>
<style scoped>
</style>