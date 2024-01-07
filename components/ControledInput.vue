<script setup>
import { ref } from "vue";

const text = ref("");
function onInput(e) {
  // v-on 핸들러는 네이티브 DOM 이벤트를 인자로 받습니다.
  text.value = e.target.value;
}

const vModelText = ref("");
</script>

<template>
  <input :value="text" @input="onInput" placeholder="여기에 입력하기" />
  <p>{{ text }}</p>
  <input v-model="vModelText" placeholder="여기에 입력하기" />
  <p>{{ vModelText }}</p>
</template>
