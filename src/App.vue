<script setup lang="ts">
import { type Ref, ref } from 'vue';
import HelloWorld from './components/HelloWorld.vue';
import TransitionEnterBasic from './transition/TransitionEnterBasic.vue';
import TransitionLeaveBasic from './transition/TransitionLeaveBasic.vue';
import MyTrasintion from './transition/MyTrasintion.vue';
import TransitinRenderInitial from './transition/TransitinRenderInitial.vue';
import TransitionMode from './transition/TransitionMode.vue';

const show: Ref<boolean> = ref(true);
const showFun = () => (show.value = !show.value);
</script>

<template>
  <HelloWorld />
  <h2>Basic</h2>
  <h3>--- enter (from, active, to)---</h3>
  <TransitionEnterBasic />
  <h3>--- leave (from, active, to)---</h3>
  <p>Nota el leave-from no se esta aplicando</p>
  <TransitionLeaveBasic />
  <h3>--- transition Reutilizable---</h3>
  <button @click="showFun">show</button>
  <MyTrasintion>
    <p v-if="show">hola</p>
  </MyTrasintion>
  <h3>--- transition en el primer render---</h3>
  <TransitinRenderInitial />
  <h3>--- transition mode---</h3>
  <TransitionMode />
</template>

<style scoped></style>
