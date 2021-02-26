<template>
  <div class="home">
    <img alt="Vue logo"
      src="../assets/logo.png">
    <!-- <HelloWorld /> -->
    <!-- <Js /> -->
    <!-- <This /> -->
    <!-- <String/> -->
    <!-- <div :style="{fontSize:postFontSize+'em'}"> -->

    <!-- <blog-post 
    v-for="post in posts"
    v-bind:key="post.id"
    v-bind:title="post.title"
    v-on:enlarge-text="postFontSize+=$event"
    >
    </blog-post> -->
    <!-- <slot-example>
      
    </slot-example>  -->

    <!-- </div> -->

    <!-- <button-counter></button-counter> -->
    <!-- <base-layout>
      <template v-slot:header>
        <h1>Header</h1>
      </template>
      <template v-slot:default>
        <h1>Content1</h1>
        <h1>Content2</h1>

      </template>
      <template v-slot:footer>
        <h1>Footer</h1>
      </template>
      <template v-slot:userName="parentUser">
        {{parentUser.user.name}}
      </template>

    </base-layout> -->
    <!-- <Event v-model="lovingVue"/> -->
    <!-- <Function/> -->
    <Closure/>
  </div>
</template>

<script>
// @ is an alias to /src
import HelloWorld from "@/components/HelloWorld.vue";
import Js from "@/components/Js.vue";
import This from "@/components/This.vue";
import String from "@/components/String.vue";
import ButtonCounter from "@/components/ButtonCounter.vue";
import BlogPost from "@/components/BlogPost.vue";
import SlotExample from "@/components/SlotExample.vue";
import BaseLayout from "@/components/BaseLayout.vue";
import Event from "@/components/Event.vue";
import Function from "@/components/Function.vue";
import Closure from "@/components/Closure.vue";

export default {
  name: "Home",
  components: {
    HelloWorld,
    Js,
    This,
    String,
    ButtonCounter,
    BlogPost,
    SlotExample,
    BaseLayout,
    Event,
    Function,
    Closure
  },
  data() {
    return {
      posts: [
        { id: 1, title: "My journey with Vue" },
        { id: 2, title: "Blogging with Vue" },
        { id: 3, title: "Why Vue is so fun" },
      ],
      postFontSize: 1,
    };
  },
};
</script>
