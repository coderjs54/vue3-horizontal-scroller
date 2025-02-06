<template>
  <div class="section__wrapper">
    <div class="section__content">{{ n }}</div>
  </div>
</template>

<script lang="ts" setup>
defineProps({
  n: Number
})
</script>

<style lang="scss" scoped>
.section__wrapper {
  cursor: pointer;
  box-sizing: border-box;
  width: 300px;
  height: 200px;
  flex-shrink: 0;
  padding: 15px;
  border-right: 2px solid yellowgreen;

  &:last-of-type {
    border-right: none;
  }

  .section__content {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: #e3e3e3;
    width: 100%;
    height: 100%;
    font-size: 30px;
  }
}
</style>