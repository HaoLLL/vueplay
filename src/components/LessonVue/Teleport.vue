<template>
  <div class="area">
    <button @click="handleClick">按钮</button>
    <teleport to="body">
      <div class="mask"
        v-show="show"></div>
    </teleport>
  </div>

</template>
<script>
// 制作蒙层
export default {
  data() {
    return {
      show: false,
    };
  },
  methods: {
    handleClick() {
      this.show = !this.show;
    },
  },
};
</script>
<style scoped>
.area {
  position: absolute;
  width: 200px;
  height: 300px;
  background: #000;
  left: 50%;
  top: 50%;
  transform: translate(-50%, -50%);
}
.mask {
  position: absolute;
  left: 0;
  top: 0;
  bottom: 0;
  right: 0;
  background: #000;
  opacity: 0.5;
}
</style>