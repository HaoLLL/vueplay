<template>
  <div class="home">
    <img alt="Vue logo"
      src="../assets/logo.png">
    <!-- <HelloWorld /> -->
    <!-- <Js /> -->
    <!-- <This /> -->
    <!-- <String/> -->
    <blog-post 
    v-for="post in posts"
    v-bind:key="post.id"
    v-bind:title="post.title">
    </blog-post>
    <!-- <button-counter></button-counter> -->
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

export default {
  name: "Home",
  components: {
    HelloWorld,
    Js,
    This,
    String,
    ButtonCounter,
    BlogPost,
  },
  data() {
    return {
      posts: [
        { id: 1, title: "My journey with Vue" },
        { id: 2, title: "Blogging with Vue" },
        { id: 3, title: "Why Vue is so fun" },
      ],
    };
  },
};
</script>
