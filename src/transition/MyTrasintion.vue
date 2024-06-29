<script setup lang="ts"></script>

<template>
  <Transition name="my-transition" class="p-interno">
    <slot></slot>
  </Transition>
</template>

<style>
.p-interno {
  color: red;
}

.my-transition-enter-active {
  transition: all 10s ease-out;
}

.my-transition-enter-from {
  transform: translateX(60px);
  color: green;
}

.my-transition-enter-to {
  transform: translateX(-60px);
  color: pink;
}
</style>
