<template>
  <div class="home">
    <p>My name is {{ name }} and my age is {{ age }}</p>
    <button @click="handleClick">Click me</button>
    <button @click="age++">add 1 to age</button>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
import { ref } from "vue";
export default {
  name: "HomeView",
  setup() {
    // const p = ref(null);

    const name = ref("Mario");
    const age = ref(30);

    const handleClick = () => {
      name.value = "engineer babu";
      age.value = 26;
    };

    return { name, age, handleClick };
  },
  data() {
    return {
      score: 5,
    };
  },
};
</script>
