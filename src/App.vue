<template>
  <div class="preview">
    <Tachometer :coefficient="position" />
  </div>
  <div>
    <button @click="position -= 0.1">-</button>
    <button @click="position += 0.1">+</button>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import Tachometer from './components/Tachometer.vue'

const position = ref(0)
</script>

<style scoped>
.preview {
  width: 300px;
  height: 300px;
  border: 2px solid;
  resize: both;
  overflow: auto;
}
</style>
