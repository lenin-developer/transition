<script setup lang="ts">
import TransitionModeDefault from './transitionMode/TransitionModeDefault.vue';
import transitionModeInOut from './transitionMode/transitionModeInOut.vue';
import TrasitionModeOutIn from './transitionMode/TrasitionModeOutIn.vue';
</script>

<template>
  <div class="wrapper">
    <TransitionModeDefault />
  </div>
  <div class="wrapper">
    <transitionModeInOut />
  </div>
  <div class="wrapper">
    <TrasitionModeOutIn />
  </div>
</template>

<style scoped>
.wrapper {
  margin-top: 40px;
}
</style>
