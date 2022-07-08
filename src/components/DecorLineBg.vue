<template>
  <div
    id="root_decor_wrapper"
    :style="{
      background: '#e96443',
      background: `-webkit-linear-gradient(to ${to}, rgba(255,0,100,1), red)`,
      background: `linear-gradient(to ${to}, rgba(255,0,100,1), red)`,
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
      <div v-if="props.to === 'right'" class="dynamic-dir-hor"></div>
      <div v-if="props.to === 'left'" class="dynamic-dir-hor-rev"></div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps([
  "reverse",
  "to",
  "top",
  "left",
  "right",
  "height",
  "width",
  "bottom",
]);
</script>

<style scoped>
.dynamic-dir {
  position: absolute;
  top: 0px;
  left: -15px;
  border-top: 20px solid orange;
  border-bottom: 20px solid rgba(0, 0, 0, 0);
  border-left: 20px solid rgba(0, 0, 0, 0);
  border-right: 20px solid rgba(0, 0, 0, 0);
  box-sizing: border-box;
  animation-name: movement1;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  opacity: 1;
}

.dynamic-dir-hor {
  position: absolute;
  top: -15px;
  left: -15px;
  border-top: 20px solid rgba(0, 0, 0, 0);
  border-bottom: 20px solid rgba(0, 0, 0, 0);
  border-left: 20px solid rgba(0, 0, 0, 0);
  border-right: 20px solid orange;
  box-sizing: border-box;
  animation-name: movement2;
  animation-duration: 2s;
  animation-iteration-count: infinite;
  opacity: 1;
}

.dynamic-dir-hor-rev {
  position: absolute;
  top: -15px;
  left: -15px;
  border-top: 20px solid rgba(0, 0, 0, 0);
  border-bottom: 20px solid rgba(0, 0, 0, 0);
  border-left: 20px solid orange;
  border-right: 20px solid rgba(0, 0, 0, 0);
  box-sizing: border-box;
  animation-name: movement3;
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

@keyframes movement2 {
  from {
    left: 100%;
    opacity: 1;
  }
  to {
    left: 0;
    opacity: 0;
  }
}

@keyframes movement3 {
  from {
    left: 0%;
    opacity: 1;
  }
  to {
    left: 100%;
    opacity: 0;
  }
}

@media only screen and (max-width: 768px) {
  #root_decor_wrapper {
    display: none;
  }
}
</style>
