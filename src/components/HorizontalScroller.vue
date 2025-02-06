<template>
  <div class="scroller__wrapper">
    <div class="scroller">
      <div class="scroller__content">
        <slot></slot>
      </div>
    </div>
  </div>
</template>

<script lang="ts" setup>

</script>

<style lang="scss" scoped>
$width: 1200px;
$height: 200px;

.scroller__wrapper {
  position: relative;
  width: $width;
  height: $height;
  border: 2px solid yellowgreen;

  .scroller {
    position: absolute;
    top: 0;
    left: 0;
    width: $height;
    height: $width;
    overflow-y: auto;
    overflow-x: hidden;
    &::-webkit-scrollbar {
      display: none;
    }
    transform: translateY($height) rotate(-90deg);
    transform-origin: left top;

    .scroller__content {
      display: flex;
      position: absolute;
      top: 0;
      left: $height;
      width: $width;
      height: $height;
      // overflow: hidden;
      transform: rotate(90deg);
      transform-origin: left top;
    }
  }
}
</style>