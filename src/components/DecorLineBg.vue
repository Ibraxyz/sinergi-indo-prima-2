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
  >
    <div
      :style="{
        position: 'relative',
        height: props.height,
        width: props.width,
      }"
    >
      <div v-if="props.to === 'bottom'" class="dynamic-dir"></div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps(["to", "top", "left", "right", "height", "width", "bottom"]);
</script>

<style scoped>
.dynamic-dir {
  position: absolute;
  top: 0px;
  left: -20px;
  border-top: 25px solid red;
  border-bottom: 25px solid rgba(0, 0, 0, 0);
  border-left: 25px solid rgba(0, 0, 0, 0);
  border-right: 25px solid rgba(0, 0, 0, 0);
  box-sizing: border-box;
  animation-name: movement1;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  opacity: 1;
}

@keyframes movement1 {
  from {
    top: 0px;
    opacity: 1;
  }
  to {
    top: 100%;
    opacity: 0;
  }
}
</style>
