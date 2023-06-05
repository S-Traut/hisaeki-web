<script setup lang="ts">
import Container from './Container.vue';
</script>

<template>
  <Container>
    <div class="header">
      <h1 class="title">ART BY HISAEKI</h1>
      <div class="links">
        <a href="">PIXIV</a>
        <a href="">INSTAGRAM</a>
      </div>
    </div>
  </Container>
</template>

<style scoped>
.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 4rem;
}

.links {
  display: flex;
  gap: 0.5rem;
  font-size: 0.8rem;
}

.title {
  font-size: 1rem;
  letter-spacing: 0.8rem;
  font-weight: 800;
}
</style>
