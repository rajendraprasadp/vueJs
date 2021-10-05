<template>
  <div>
    <h4>tab c content</h4>
    <input type="text" v-model="name" />
  </div>
</template>

<script>
export default {
  name: "TabC",
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style scoped></style>
