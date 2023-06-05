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
  }
});

function getImageUrl() {
  return new URL(`../../assets/images/${props.src}`, import.meta.url).href
}
</script>

<template>
  <div class="bp-wrapper">
    <img ref="image" :src="getImageUrl()" />
  </div>
</template>

<style scoped>
.bp-wrapper {
  height: calc(100vh - 8rem);
  overflow: hidden;
}

img {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
</style>
