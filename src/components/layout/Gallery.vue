<script setup lang="ts">
defineProps({
  images: {
    type: Array<string>,
    required: true,
  },
});

function getImageUrl(image: string) {
  return new URL(`../../assets/images/${image}`, import.meta.url).href
}
</script>

<template>
  <masonry-wall :items="images" :ssr-columns="4" :gap="10">
    <template #default="{ item, index }">
        <div class="image-wrapper" :src="item">
            <img :src="getImageUrl(item)" alt="">
        </div>
    </template>
  </masonry-wall>
</template>

<style scoped>
.gallery {
  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  gap: 1rem;
}

.image-wrapper {
    overflow: hidden;
    display: flex;
    align-items: center;
    justify-content: center;
}

.image-wrapper > img {
    width: 100%;
    height: auto;
}
</style>
