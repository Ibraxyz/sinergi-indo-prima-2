<template>
  <h1 v-if="variant === 'h1'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h1>
  <h2 v-if="variant === 'h2'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h2>
  <h3 v-if="variant === 'h3'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h3>
  <h4 v-if="variant === 'h4'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h4>
  <h5 v-if="variant === 'h5'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h5>
  <h6 v-if="variant === 'h6'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </h6>
  <p v-if="variant === 'p'" :class="props.mode" :style="props.sx">
    <slot></slot>
  </p>
  <span v-if="variant === 'span'" :class="props.mode" :style="props.sx"
    ><slot></slot
  ></span>
</template>

<script setup>
const props = defineProps(["variant", "mode", "sx"]);
</script>

<style scoped>
h1,
h2,
h3,
h4,
h5,
h6,
p,
span {
  font-family: "Montserrat", sans-serif;
}

.light {
  color: #ffffff;
}

.dark {
  color: #000000;
}

p {
  font-size: 20px;
  font-weight: 100;
}
</style>
