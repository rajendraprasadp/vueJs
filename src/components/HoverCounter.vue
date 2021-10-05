<template>
  <div>
    <h1 @mouseover="incrementCount">hovered {{ count }} times</h1>
  </div>
</template>

<script>
import useCounter from "../composables/usecounter";
// import Mixin from "../mixins/counter";
export default {
  name: "HoverCounter",
  setup() {
    const { count, incrementCount } = useCounter();

    return {
      count,
      incrementCount,
    };
  },
  // mixins: [Mixin],
};
</script>

<style scoped></style>
