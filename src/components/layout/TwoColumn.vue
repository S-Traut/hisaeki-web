<script setup lang="ts"></script>

<template>
  <div class="two-column">
    <div>
      <slot name="left-col" />
    </div>
    <div>
      <slot name="right-col" />
    </div>
  </div>
</template>

<style scoped>
.two-column {
  display: inline;
}
@media screen and (min-width: 1080px) {
  .two-column {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
</style>
