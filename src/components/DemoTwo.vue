<template>
  <div>
    <h1>{{ state.firstName }} {{ state.lastName }}</h1>
  </div>
</template>

<script >
import { reactive } from "vue";
export default {
  name: "DemoTwo",
  setup() {
    const state = reactive({
      firstName: "raj",
      lastName: "noob",
    });

    setTimeout(() => {
      state.firstName = "noob";
      state.lastName = "nodsdsdsadob"
      console.log(state);
    }, 2000);
    return {
      state,
    };
  },
};
