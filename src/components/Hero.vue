<template>
  <div class="wrapper">
    <div class="bg-wrapper">
      <slot name="background"></slot>
    </div>
    <div class="overlay">
      <slot name="content"></slot>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.wrapper {
  width: 100%;
  height: 100vh;
  position: relative;
}

.bg-wrapper {
  width: 100%;
  height: 100%;
  position: absolute;
  top: 0px;
  left: 0px;
  z-index: 1;
}

.overlay {
  position: absolute;
  width: 100%;
  height: 100%;
  top: 0px;
  left: 0px;
  z-index: 2;
  background-image: linear-gradient(
    to bottom,
    rgba(0, 0, 0, 0.8),
    rgba(0, 0, 0, 0.1)
  );
}
</style>
