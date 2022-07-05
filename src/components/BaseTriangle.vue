<template>
  <div class="triangle" :style="computedStyle"></div>
</template>

<script setup>
import { computed } from "vue";
const props = defineProps(["position"]);

const computedStyle = computed(() => {
  let style = {
    "border-top": `20px solid ${
      props.position === "top" ? "rgba(255, 0, 100, 1)" : "rgba(0, 0, 0, 0)"
    }`,
    "border-bottom": `20px solid ${
      props.position === "bottom" ? "rgba(255, 0, 100, 1)" : "rgba(0, 0, 0, 0)"
    }`,
    "border-left": `20px solid ${
      props.position === "left" ? "rgba(255, 0, 100, 1)" : "rgba(0, 0, 0, 0)"
    }`,
    "border-right": `20px solid ${
      props.position === "right" ? "rgba(255, 0, 100, 1)" : "rgba(0, 0, 0, 0)"
    }`,
  };
  return style;
});
</script>

<style scoped>
.triangle {
  width: 0px;
  height: 0px;
}
</style>
