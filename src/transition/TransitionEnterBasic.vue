<script setup lang="ts">
import { type Ref, ref } from 'vue';

const show: Ref<boolean> = ref(true);
const showFun = () => (show.value = !show.value);
</script>

<template>
  <button @click="showFun">show</button>
  <Transition>
    <p v-if="show">hola</p>
  </Transition>
</template>

<style scoped>
p {
  color: green;
}

.v-enter-active {
  transition: all 3s ease-out;
}

.v-enter-from {
  transform: translateX(60px);
  color: red;
}

.v-enter-to {
  transform: translateX(-60px);
  color: yellow;
}
</style>
