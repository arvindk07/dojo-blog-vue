<template>
  <div class="home">
    <p>
      My name is <b>{{ name }}</b> and my age is <b> {{ age }}</b>
    </p>
    <button @click="handleClick">Click me</button>
  </div>
</template>

<script>
export default {
  name: "HomeView",
  setup() {
    console.log("setup");

    let name = "Mario";
    let age = 30;

    const handleClick = () => {
      console.log("You Clicked me");
    };

    return { name, age, handleClick };
  },
};
</script>
