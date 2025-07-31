<template>
  <h2>My Course Goal</h2>
  <!-- Task 1: Output your main course goal with help of the composition API -->
  <!-- Don't hardcode it into the template, instead hardcode it into the JS code -->
  <h3 v-if="goalShown">{{ goal }}</h3>
  <!-- Task 2: Toggle (show/ hide) the goal with help of the button  -->
  <button @click="toggleGoal">Toggle Goal</button>
  <!-- Task 3: Manage data in three ways -->
  <!-- => Separate refs -->
  <!-- => Ref Object -->
  <!-- => Reactive Object -->
  <!-- Task 4: Also solve the assignment with the Options API -->
</template>

<script setup>
import {ref, reactive, computed} from "vue";

// const goal = ref('Be A Master Coder!');
const goals = reactive({
  goal: 'Be A Master Coder!',
  goalShown: false
});

function toggleGoal() {
  goals.goalShown = !goals.goalShown;
}

const goal = computed(() => goals.goal)
const goalShown = computed(() => goals.goalShown)
// export default {
//   data() {
//     return {
//       goal: 'Be A Master Coder!',
//       goalShown: false
//     }
//   },
//   methods: {
//     toggleGoal() {
//       this.goalShown = !this.goalShown
//     }
//   }
// }
</script>

<style>
html {
  font-family: sans-serif;
}
body {
  margin: 3rem;
  text-align: center;
}
</style>