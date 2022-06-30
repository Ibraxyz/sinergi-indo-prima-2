<template>
  <div
    :style="{
      background: '#e96443',
      background: `-webkit-linear-gradient(to ${to}, #e96443, #904e95)`,
      background: `linear-gradient(to ${to}, #e96443, #904e95)`,
      position: 'absolute',
      top: props.top,
      left: props.left,
      right: props.right,
      height: props.height,
      bottom: props.bottom,
      width: props.width,
    }"
  ></div>
</template>

<script setup>
const props = defineProps(["to", "top", "left", "right", "height", "width", "bottom"]);
</script>

<style scoped></style>
