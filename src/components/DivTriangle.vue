<template>
  <!--  #f3f8fb -->
  <div
    class="triangle"
    :style="{
      top: props.top ? props.top : '-50px',
      left: props.left ? props.left : '-50px',
      right: props.right ? props.right : '-50px',
      transform: props.rotate ? `rotate(${props.rotate}deg)` : `rotate(${-45}deg)`,
      'border-bottom': `${props.big ? props.big : 50}px solid ${
        props.bgColor ? props.bgColor : '#f3f8fb'
      }`,
      'border-top': `${props.big ? props.big : 50}px solid rgba(0, 0, 0, 0)`,
      'border-left': `${props.big ? props.big : 50}px solid rgba(0, 0, 0, 0)`,
      'border-right': `${props.big ? props.big : 50}px solid rgba(0, 0, 0, 0)`,
    }"
  ></div>
</template>

<script setup>
const props = defineProps(["bgColor", "rotate", "top", "left", "right", "big"]);
</script>

<style scoped>
.triangle {
  width: 0px;
  height: 0px;
  position: absolute;
  z-index: 8;
}
</style>
