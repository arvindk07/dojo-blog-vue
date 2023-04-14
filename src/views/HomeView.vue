<template>
  <div class="home">
    <h1>Home</h1>
    <PostList v-if="showPosts" :posts="posts" />
    <button @click="showPosts = !showPosts">Toggle Post</button>
    <button @click="posts.pop()">Delete Post</button>
  </div>
</template>

<script>
import { ref, computed, watch, watchEffect } from "vue";
import PostList from "@/components/PostList.vue";
export default {
  name: "HomeView",
  components: {
    PostList,
  },
  setup() {
    const posts = ref([
      { title: "Welcome to the blog", body: "lorem ipsum", id: 1 },
      { title: "Top 5 css", body: "lorem ipsum", id: 2 },
    ]);
    const showPosts = ref(true);

    return { posts, showPosts };
  },
};
</script>
