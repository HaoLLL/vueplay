<template>
  <div class="home">
    <img alt="Vue logo" src="../assets/logo.png">
    <!-- <HelloWorld /> -->
    <Js />
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from '@/components/HelloWorld.vue'
import Js from '@/components/Js.vue'

export default {
  name: 'Home',
  components: {
    HelloWorld,
    Js
  }
}
</script>
