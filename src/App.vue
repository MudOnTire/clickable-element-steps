<template>
  <div id="app">
    <clickable-steps :space="200" :active="1" finish-status="success" @click="onStepClick">
      <clickable-step title="步骤 1"></clickable-step>
      <clickable-step title="步骤 2"></clickable-step>
      <clickable-step title="步骤 3"></clickable-step>
    </clickable-steps>
  </div>
</template>

<script>
import ClickableSteps from "./components/steps/clickable-steps";
import ClickableStep from "./components/steps/clickable-step";

export default {
  name: "app",
  components: {
    "clickable-steps": ClickableSteps,
    "clickable-step": ClickableStep
  },
  methods: {
    onStepClick(step) {
      console.log(step);
    }
  }
};
</script>

<style>
</style>
