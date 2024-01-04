<script setup>
import { ref } from "vue";

const count = ref(0);

const increment = () => {
  count.value++;
};
</script>

<template>
  <!-- make this button work -->
  <button @click="increment">count is: {{ count }}</button>
  <button v-on:click="increment">count is: {{ count }}</button>
</template>
