<template>
    <img class="image" :src="getImageUrl()" :alt="alt">
</template>

<script setup lang="ts">
const props = defineProps({
    src: String,
    alt: String,
});

function getImageUrl() {
  return new URL(`../../assets/images/${props.src}`, import.meta.url).href;
}
</script>

<style scoped>
.image {
    width: 100%;
    height: 100%;
}
</style>