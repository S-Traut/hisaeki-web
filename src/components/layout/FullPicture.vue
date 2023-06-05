<script setup lang="ts">
import { onMounted, ref } from "vue";
import simpleParallax from "simple-parallax-js";

const props = defineProps({
  src: {
    required: true,
    type: String,
  },
});

const image = ref<HTMLDivElement>();
onMounted(() => {
  if (image.value) {
    new simpleParallax(image.value, {delay: 1, scale: 1.2});
  }
});

function getImageUrl() {
  return new URL(`../../assets/images/${props.src}`, import.meta.url).href
}
</script>

<template>
  <div class="fp-wrapper">
    <img ref="image" :src="getImageUrl()" />
  </div>
</template>

<style scoped>
.fp-wrapper {
    width: 100%;
    height: 600px;
    overflow: hidden;
    display: flex;
    justify-content: center;
}

img {
    width: 100%;
    height: auto;
}
</style>
