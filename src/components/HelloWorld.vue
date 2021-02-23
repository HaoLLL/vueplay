<template>
  <!-- v-if;  v-bind; v-on; v-model-->
  <!-- v-bind:class -->
  <!-- add v-if to template: a group of v-if-->
  <!--  template key-->


  <!-- data(); computed; methods; watch  -->
  <!-- 1. computed properties for complicated log -->
  <!-- computed/methods -->
  <!-- 2. watch -->
  <div class="hello">
    <template v-if="show">
      <h1>Title</h1>
      <p>Paragraph 1</p>
      <p>Paragraph 2</p>
    </template>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  data() {
    return {
      message: "Hello world",
      seen: true,
      classObject: {
        active: true,
        "text-danger": true,
      },
      show: true,
    };
  },
  computed: {
    reverseMessage: function () {
      return this.message.split("").reverse().join();
    },
  },
  methods: {
    // reverseMessage:function(){
    //   return this.message.split('').reverse().join();
    // }
  },
  watch: {},
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
