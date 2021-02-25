<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld /> -->
    <!-- <Js /> -->
    <This />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Js from '@/components/Js.vue'
import This from '@/components/This.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Js,
    This
  }
}
</script>
