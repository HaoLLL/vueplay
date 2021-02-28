<template>
  <div>
    <!-- <form action="http://www.baidu.com.cn"
      @click.prevent="handleClick">
      <button type="submit">提交</button>
    </form>
    {{total}} -->
    {{number}}
  </div>

</template>
<script>
// arrow function point to window
// computed 属性！！！！！！VS methods
// 只有依赖的数值变化
// 只要页面重新渲染 就会执行
// Date.now() 测试
// watcher: wait 5s async process
// computed watch: sync使用computed
// Non-prop <div msg="hello"></div>

const myMixin = {
  data() {
    return { number: 2 };
  },
  created () {
      console.log("mixin created");
  }
};
export default {
  inheritAttrs: false,
  mixins: [myMixin],
  props: {
    // msg:{
    //     required:true,
    //     default:'message'
    // }
  },
  data() {
    return {
      price: 5,
      count: 2,
    };
  },
  computed: {
    total() {
      return this.price * this.count;
    },
  },
  created(){
      console.log("common created");
  },
  methods: {
    handleClick(e) {},
  },
  watch: {
    price(current, prev) {
      setTimeout(() => {
        console.log("price change", prev, current);
      }, 3000);
    },
  },
};
</script>
<style scoped>
</style>