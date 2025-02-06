<script setup lang="ts">
import HorizontalScroller from './components/HorizontalScroller.vue'
import Section from './components/Section.vue'
</script>

<template>
  <div>
    <h1>纯CSS实现水平方向滚动的容器</h1>
    <h2>将鼠标放置在容器上然后滚动鼠标滚轮</h2>
    <HorizontalScroller>
      <Section v-for="i in 16" :n="i" />
    </HorizontalScroller>
  </div>
</template>

<style scoped>

</style>
