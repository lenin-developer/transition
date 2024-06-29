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
  transform: translateX(0);
  color: green;
}

.v-leave-active {
  transition: all 5s ease-out;
}

.v-leave-from {
  transform: translateX(60px);
  color: red;
}

.v-leave-to {
  transform: translateX(-60px);
  color: yellow;
}
</style>
