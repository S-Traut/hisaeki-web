<script setup lang="ts">
import { RouterLink } from 'vue-router';
import Container from './Container.vue';
</script>

<template>
  <Container>
    <div class="header">
      <RouterLink to="/"><h1 class="title">ART BY HISAEKI</h1></RouterLink>
      <div class="links">
        <a href="https://www.instagram.com/hisae.ki">INSTAGRAM</a>
        <a href="https://www.pixiv.net/en/users/44549352">PIXIV</a>
        <a href="https://twitter.com/Hisaeki">TWITTER</a>
        <RouterLink to="/contact">CONTACT</RouterLink>
      </div>
    </div>
  </Container>
</template>

<style scoped>
@media screen and (max-width: 720px) {
  .header {
    margin-top: 4rem;
    margin-bottom: 4rem;
    flex-direction: column-reverse;
    text-align: center;
  }

  .header h1 {
    font-size: 0.8rem;
  }
}

.header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  height: 4rem;
}

.links {
  display: flex;
  justify-content: center;
  flex-wrap: wrap;
  gap: 0.5rem;
  font-size: 0.8rem;
}

.title {
  color: var(--vt-c-black);
  font-size: 1rem;
  letter-spacing: 0.8rem;
  font-weight: 800;
}
</style>
