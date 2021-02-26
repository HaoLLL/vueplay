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
// props: parent to children
// $emit()   $event()   children to parent
// slot parent to children
// slot children to parent

// 1.template + v-slot:header  ->  name
// 2.具名插槽 name="header" -> #header
// 3.作用域插槽 父组件想要用子组件中的data 
// slot上面的attribute是插槽prop v-bind将user带到上面去 并且取了另一个名字
// 4.解构插槽
// 5.动态插槽名 parent v-slot:[dynamicSlotName]
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