<script setup lang="ts">
const props = defineProps<{
  align: CanvasTextAlign;
  text: string;
}>();

function get_bar_class() {
    switch(props.align) {
        case 'left': return {'left-bar': true};
        case 'center': return {'center-bar': true};
        case 'right': return {'right-bar': true};
        default: return {'left-bar': true};
    }
}
</script>

<template>
  <h2 :style="{ textAlign: align }" class="mb-2 title" :class="get_bar_class()">{{ text }}</h2>
</template>

<style scoped>
.title {
  font-size: 0.8rem;
  letter-spacing: 0.8rem;
  position: relative;
  margin-bottom: 2rem;
}

.left-bar::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -0.5rem;
  width: 30px;
  height: 2px;
  background-color: var(--vt-c-black);
}
.center-bar::after {
  content: "";
  position: absolute;
  left: calc(50% - 30px);
  bottom: -0.5rem;
  width: 60px;
  height: 2px;
  background-color: var(--vt-c-black);
}

.right-bar::after {
  content: "";
  position: absolute;
  left: 0;
  bottom: -0.5rem;
  width: 30px;
  height: 2px;
  background-color: var(--vt-c-black);
}
</style>
