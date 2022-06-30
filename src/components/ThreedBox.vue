<template>
  <div class="row">
    <div class="box">
      <slot></slot>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.row {
  display: flex;
  justify-content: center;
  perspective: 30px;
}

.box {
  box-sizing: border-box;
  width: 100%;
  margin: 0 2em;
  padding: 60px 0;
  text-align: center;
  /** background-color: hsl(150, 50%, 40%); **/
  transform: rotateY(-10deg);
}
</style>
