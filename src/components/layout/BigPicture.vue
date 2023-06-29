<script setup lang="ts">
import { onMounted, ref } from "vue";

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
  return new URL(`../../assets/images/${props.src}`, import.meta.url).href;
}
</script>

<template>
  <div class="bp-wrapper">
    <img ref="image" :src="getImageUrl()" />
  </div>
</template>

<style scoped>
.bp-wrapper {
  display: none;
  height: 600px;
  overflow: hidden;
}

img {
  width: 100%;
  height: auto;
}

@media screen and (min-width: 720px) {
  .bp-wrapper {
    display: block;
    height: 600px;
  }
}

@media screen and (min-width: 1080px) {
  .bp-wrapper {
    height: calc(100vh - 8rem);
  }
}
</style>
