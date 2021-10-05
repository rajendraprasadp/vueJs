<template>
  <div>
    <input type="text" placeholder="First name" v-model="fName" />
    <input type="text" placeholder="last name" v-model="lName" />
    <h2>options fullname {{ fullName }} {{ lastName }}</h2>

    <input type="text" placeholder="First name" v-model="rfN" />
    <input type="text" placeholder="last name" v-model="rlN" />
    <h2>composition fullname {{ rfN }} {{ lfN }}</h2>
  </div>
</template>

<script>
import { ref, computed } from "vue";

export default {
  name: "Computed",
  setup() {
    const rfN = ref("");
    const rlN = ref("");

    const rfuN = computed(function() {
      return ` ${rfN.value}${lfN.value}`;
    });

    return {
      rfN,
      rlN,
      rfuN,
    };
  },

  //   data() {
  //     return {
  //       fName: "",
  //       lName: "",
  //     };
  //   },
  //   computed: {
  //     fullName() {
  //       return `${this.fName} ${this.lName}`;
  //     },
  //   },
};
</script>

<style scoped></style>
