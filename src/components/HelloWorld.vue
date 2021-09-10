<script setup lang="ts">
import { ref } from 'vue'

defineProps<{ msg: string }>()

const count = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>
  <div class="container">
    Wont work:
    <img src="/alert-octagon.svg" alt />
  </div>
  <div class="container">
    Works:
    <img :src="'/alert-octagon.svg'" alt />
  </div>
  <div>
    After that, try commenting the first image and try running yarn build again
  </div>
</template>

<style scoped>

.container {
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
