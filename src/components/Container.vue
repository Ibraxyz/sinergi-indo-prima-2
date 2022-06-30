<template>
  <div class="noPadding ? container : container-no-padding">
    <slot></slot>
  </div>
</template>

<script setup>
const props = defineProps(["noPadding"]);
</script>

<style scoped>
.container {
  box-sizing: border-box;
  max-width: 1110px;
  margin: auto;
  padding: 15px;
}

.container-no-padding {
  box-sizing: border-box;
  max-width: 1110px;
  margin: auto;
}
</style>
