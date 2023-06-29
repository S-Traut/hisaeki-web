<template>
  <div class="pp-container">
    <img :src="getImageUrl()" :alt="alt" />
  </div>
</template>

<script setup lang="ts">
const props = defineProps({
  src: String,
  alt: String,
  width: Number,
  height: Number,
});

function getImageUrl() {
  return new URL(`../../assets/images/${props.src}`, import.meta.url).href;
}
</script>

<style scoped>
.pp-container {
  overflow: hidden;
  width: 300px;
  height: 300px;
  border-radius: 50%;
}

.pp-container > img {
  width: 100%;
  height: 100%;
}
</style>
