<template>
  <div class="container" :class="{ fh: fullHeight }">
    <slot />
  </div>
</template>

<script setup lang="ts">
defineProps({
  fullHeight: Boolean,
});
</script>

<style scoped>
.container {
  max-width: 2440px;
  margin-left: auto;
  margin-right: auto;
}

@media screen and (min-width: 720px) {
  .fh {
    height: calc(100vh - 8rem);
    display: flex;
    align-items: center;
    justify-content: center;
    max-height: 1080px;
  }
}
</style>
