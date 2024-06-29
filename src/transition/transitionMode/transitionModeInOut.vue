<script setup>
import { ref } from 'vue';

const docState = ref('saved');
</script>

<template>
  <span>mode: in-out</span>
  <div class="btn-container">
    <Transition name="slide-up" mode="in-out">
      <button v-if="docState === 'saved'" @click="docState = 'edited'">
        Edit
      </button>
      <button v-else-if="docState === 'edited'" @click="docState = 'editing'">
        Save
      </button>
      <button v-else-if="docState === 'editing'" @click="docState = 'saved'">
        Cancel
      </button>
    </Transition>
  </div>
</template>

<style scoped>
.btn-container {
  display: inline-block;
  position: relative;
  height: 1em;
}

button {
  position: absolute;
}

.slide-up-enter-active,
.slide-up-leave-active {
  transition: all 0.25s ease-out;
}

.slide-up-enter-from {
  opacity: 0;
  transform: translateY(30px);
}

.slide-up-leave-to {
  opacity: 0;
  transform: translateY(-30px);
}
</style>
