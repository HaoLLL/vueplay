<template>
  <div class="container">
    <header>
      <slot name="header"></slot>
    </header>
    <main>
      <slot></slot>
    </main>
    <footer>
      <slot name="footer"></slot>
    </footer>

    <span>
      <slot name="userName" v-bind:user="user">
        {{user.name}}
      </slot>
    </span>
  </div>

</template>
<script>
// 1.template + v-slot:header  ->  name
// 2.具名插槽
// 3.作用域插槽 父组件想要用子组件中的data 
// slot上面的attribute是插槽prop v-bind将user带到上面去 并且取了另一个名字
// 
export default {
    data(){
        return  {
            user:{
                name:'Lei'
            }
        }
    }
};
</script>
<style scoped>
</style>