<template>
  <div class="home">
    <h2>Refa</h2>
    <p>
      My name is {{ enngineerBabu.name }} and my age is {{ enngineerBabu.age }}
    </p>
    <button @click="updateEngineerBabu">Update Engineer Babu</button>
    <h2>Reactive</h2>
    <p>
      My name is {{ enngineerBabuReactive.name }} and my age is
      {{ enngineerBabuReactive.age }}
    </p>
    <button @click="updateReactive">Update Engineer Babu Reactive</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "HomeView",
  setup() {
    // const p = ref(null);

    const enngineerBabu = ref({ name: "Mario", age: 30 });
    const enngineerBabuReactive = reactive({ name: "Dev", age: 35 });

    const updateEngineerBabu = () => {
      enngineerBabu.value.age = 26;
    };
    const updateReactive = () => {
      enngineerBabuReactive.age = 25;
    };

    return {
      enngineerBabu,
      updateEngineerBabu,
      enngineerBabuReactive,
      updateReactive,
    };
  },
};
</script>
