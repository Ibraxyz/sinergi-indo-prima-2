<template>
  <div
    style="
      position: relative;
      width: 80%;
      height: auto;
      box-sizing: border-box;
      z-index: 100;
      background-image: linear-gradient(to right, rgba(255, 0, 100, 1), red);
      padding: 10px;
    "
  >
    <img :src="props.img" alt="" style="width: 100%; height: auto" />
  </div>
</template>

<script setup>
const props = defineProps(["img"]);
</script>

<style scoped></style>
