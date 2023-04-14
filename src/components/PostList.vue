<template>
  <div class="post-list">
    <div v-for="post in posts" :key="post.id"><SinglePost :post="post" /></div>
  </div>
</template>

<script>
import { onMounted, onUnmounted, onUpdated } from "vue";
import SinglePost from "./SinglePost.vue";
export default {
  props: ["posts"],

  components: { SinglePost },
  setup(props) {
    onMounted(() => console.log("component mounted"));
    onUnmounted(() => console.log("component unmounted"));
    onUpdated(() => console.log("components updated"));
  },

  mounted() {
    console.log("mounted using options api");
  },

  unmounted() {
    console.log("unmounted using options api");
  },

  updated() {
    console.log("updated using options api");
  },
};
</script>

<style></style>
