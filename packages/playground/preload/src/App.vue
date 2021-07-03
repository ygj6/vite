<template>
  <div>This is app page</div>
  <button type="button" @click="show = !show">show</button>
  <div v-if="show">
    <about />
  </div>
</template>

<script setup>
import { ref, defineAsyncComponent } from 'vue'
const About = defineAsyncComponent(() => import('./About.vue'))
const show = ref(false)
</script>
