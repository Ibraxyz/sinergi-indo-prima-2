<template>
  <div>
    <slot></slot>
  </div>
</template>

<script setup>
import DivTriangle from "./DivTriangle.vue";
</script>

<style scoped>
.decor-wrapper {
  position: relative;
  top: -40px;
  width: 100%;
  height: 40px;
  z-index: 10;
  box-sizing: border-box;
}

.col1 {
  display: inline-block;
  width: 50%;
  height: 40px;
  box-sizing: border-box;
}
.col2 {
  display: inline-block;
  width: 50%;
  height: 40px;
  box-sizing: border-box;
  text-align: right;
}

.decor-wrapper img {
  max-width: 100%;
  height: 40px;
}
</style>
