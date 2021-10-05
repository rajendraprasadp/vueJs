<template>
  <div>
    <h2>article component</h2>
    <h2>{{ title }}</h2>
    <h1>{{ uname }}</h1>

    <h2>likes-{{ likes }}</h2>
    <h2>publishged-{{ isPublished ? "yes" : "no" }}</h2>
  </div>
</template>

<script>
export default {
  name: "Article",
  inject: ["uname"],
  props: {
    title: {
      type: String,
      required: true,
      default: "Article default value",
    },
    likes: Number,
    isPublished: Boolean,
  },
};
</script>

<style scoped></style>
