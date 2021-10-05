<template>
  <div>
    <h1>{{ name }}</h1>
    <button @click="setName">change name</button>

    <h2>{{ count }}</h2>
    <button @click="incrementCount">increment count</button>

    <h2>{{ state.first }} {{ state.last }}</h2>
    <button @click="ChangeHero">change hero</button>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "Methods",
  setup() {
    const count = ref(0);
    const state = reactive({
      first: "Bruce",
      last: "Wayne",
    });

    function incrementCount() {
      count.value++;
    }

    function ChangeHero() {
      state.first = "noo";
      state.last = "your";
    }
    return {
      count,
      incrementCount,
      state,
      ChangeHero,
    };
  },

  data() {
    return {
      name: "vishwas",
    };
  },
  methods: {
    setName() {
      this.name = "codeEvolution";
    },
  },
};
</script>

<style scoped></style>
