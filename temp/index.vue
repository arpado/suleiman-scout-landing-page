<template>
  <hero-section />
</template>

<script>
import HeroSection from './HeroSection.vue'
export default {
  components: { HeroSection },
  name: 'IndexPage'
}
</script>

<style>
@import './augmented-ui.min.css';

:root {
  --main-darkblue: #285278;
  --main-lightblue: #afd3ff;
  --main-yellow: #e09f20;
  --main-white: #f1f1e6;
  --main-black: #303437;
}
</style>
