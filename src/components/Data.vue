<template>
  <div>
    <h2>options -{{ o_firstName }}</h2>
    <h2>Composition -{{ c_firstName }}</h2>
    <h2>Composition -{{ greet }}</h2>
    <h2>
      Composition reac -{{ state.firstName }}{{ state.secondName
      }}{{ state.heroName }}
    </h2>
    <h2>Composition reac -{{ reactivee }}</h2>

    <h2>
      composition -{{ c_lastName }} {{ c_firstName }} a ka {{ c_heroName }}
    </h2>
  </div>
</template>

<script>
import { ref, reactive } from "vue";
export default {
  name: "Data",
  setup() {
    const c_firstName = ref("Clak");
    const c_lastName = ref("kent");
    const c_heroName = ref("super");

    const greet = `hello ${c_firstName.value}`;
    const greetHero = `hello ${c_firstName.value}${c_lastName.value} aka ${c_heroName.value}   `;

    const state = reactive({
      firstName: "how",
      secondName: "are",
      heroName: "you",
    });

    const reactivee = `hello ${state.firstName} ${state.secondName}  aka ${state.heroName} `;
    return {
      c_firstName,
      greet,
      greetHero,
      c_lastName,
      c_heroName,
      state,
      reactivee,
    };
  },
  data() {
    return {
      o_firstName: "Bruce",
    };
  },
};
</script>

<style scoped></style>
