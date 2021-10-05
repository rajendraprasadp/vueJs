<template>
  <div>
    <button @click="incrementCount">clicked {{ count }} times</button>
  </div>
</template>

<script>
import useCounter from "../composables/usecounter";
// import Countermixin from "../mixins/counter";
export default {
  name: "ClickCounter",
  setup() {
    const { count, incrementCount } = useCounter();

    return {
      count,
      incrementCount,
    };
  },

  // mixins: [Countermixin],
};
</script>

<style scoped></style>
