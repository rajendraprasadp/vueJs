<template>
  <div>
    <h1>this is popup</h1>
    <input type="text" v-model="name" />

    <button @click="$emit('close', name)">close popup</button>
  </div>
</template>

<script>
export default {
  name: "Popup",
  emit: ["close"],
  data() {
    return {
      name: "",
    };
  },
};
</script>

<style scoped></style>
