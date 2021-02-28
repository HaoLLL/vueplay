<template>
  <div id="basicVue">
    <div>{{message}}</div>
    <button v-on:click="change">sdfa</button>

  </div>

</template>
<script>
export default {
  data() {
    return {
      message: "basicVue",
    };
  },
  methods: {
    change() {
      this.message = "asg";
    },
  },
  // 实例生成之前会自动执行的函数
  beforeCreate() {
    console.log("beforeCreate");
  },
  //   实例生成之后
  created() {
    console.log("created");
  },
  //   组件渲染到页面之前 模板被编译成函数
  beforeMount() {
    console.log(document.getElementById("basicVue").innerHTML, "beforeMount");
  },
  //   if has template
  // 1. to a render function

  //   内容挂载到页面上
  mounted() {
    console.log(document.getElementById("basicVue").innerHTML, "mounted");
  },

  //   数据发生变化 vm.$data.message = 'bye'
  beforeUpdate() {
    console.log(document.getElementById("basicVue").innerHTML, "beforeUpdate");
  },
  // data中的数据发生变化 页面完成更新以后
  updated() {
    console.log(document.getElementById("basicVue").innerHTML, "updated");
  },
//   Vue应用失效的时候
  beforeUnmount(){
    console.log(document.getElementById("basicVue").innerHTML, "beforeUnmount");
  },
//   dom完全销毁之后
  unmounted(){
    console.log(document.getElementById("basicVue").innerHTML, "unmounted");
  }

};
</script>
<style scoped>
</style>