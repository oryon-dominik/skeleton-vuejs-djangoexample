<template>
  <h1>Vue Application</h1>
  <div class="flex justify-center">
    <img class="logo" src="https://vuejs.org/logo.svg" alt="vuejs-logo">
  </div>
  <ExampleComponent :message="`${message}`" />
</template>

<script setup lang="ts">
import { ref } from 'vue'
import ExampleComponent from './components/ExampleComponent.vue'

const _vueMessage = document.getElementById("vue-message")
const _message: string = (_vueMessage == null || _vueMessage.textContent == null) ? "" : JSON.parse(_vueMessage.textContent)
const message = ref(_message)

</script>

<style scoped>
.logo {
  height: 6em;
  padding: 1.5em;
  will-change: filter;
  transition: filter 300ms;
}
.logo:hover {
  filter: drop-shadow(0 0 2em #646cffaa);
}
.logo.vue:hover {
  filter: drop-shadow(0 0 2em #42b883aa);
}

</style>
