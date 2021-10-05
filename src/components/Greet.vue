<template>
  <h2>hello {{ name }} a.k.a {{ hn }}</h2>
</template>

<script>
export default {
  name: "Greet",
  props: ["name", "hn"],
};
</script>

<style scoped></style>
