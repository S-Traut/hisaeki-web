
<template>
  <div class="two-column" :class="{fh: fullHeight, invert: invert}">
    <div>
      <slot name="left-col" />
    </div>
    <div>
      <slot name="right-col" />
    </div>
  </div>
</template>

<script setup lang="ts">
defineProps({
  fullHeight: Boolean,
  invert: Boolean
})
</script>

<style scoped>
.two-column {
  display: inline;
}

.invert {
  display: flex;
  flex-direction: column-reverse;
  justify-content: center;
  align-items: center;
}


@media screen and (min-width: 370px) {
    .fh {
      height: calc(100vh - 4rem);
      max-height: 1080px;
    }
}

@media screen and (min-width: 1080px) {
  .two-column {
    display: grid;
    grid-template-columns: 1fr 1fr;
  }
}
</style>
