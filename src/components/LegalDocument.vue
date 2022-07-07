<template>
  <div class="wrapperx">
    <!-- card -->
    <div class="card red-glow">
      <img :src="props.info.img" alt="" style="width: 100%; height: auto" />
    </div>

    <!-- card shadow -->
    <div class="card-shadow">
      <div class="card-shadow-content-holder">
        <img
          :src="props.info.img"
          alt=""
          style="
            width: 100%;
            height: auto;
            position: relative;
            top: -130px;
            -webkit-transform: scaleX(-1);
            transform: scaleX(-1);
          "
        />
      </div>
      <div class="card-shadow-gradient"></div>
    </div>
  </div>
</template>

<script setup>
import Legal1 from "../assets/legal1.png";
const props = defineProps(["info"]);
</script>

<style scoped>
.wrapperx {
  width: 100%;
  height: 400px;
  /** background-image: linear-gradient(to top, rgb(2, 11, 74), rgba(0, 0, 0, 0)); **/
  position: relative;
}
.card {
  width: 200px;
  height: 275px;
  background-color: #ffffff;
  margin: auto;
  position: relative;
  z-index: 2;
  border-radius: 5px;
  overflow: hidden;
}
.card-shadow {
  width: 200px;
  height: 100px;
  margin: auto;
  position: relative;
  z-index: 2;
  border-radius: 5px;
  overflow: hidden;
}
.card-shadow-content-holder {
  width: 100%;
  height: 100%;
  background-color: #ffffff;
  border-radius: 5px;
  overflow: hidden;
  opacity: 0.3;
  margin-top: 5px;
  transform: rotate(180deg);
}
.card-shadow-gradient {
  background-image: linear-gradient(to top, rgb(2, 11, 74), rgba(0, 0, 0, 0));
  position: absolute;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
}
.red-glow {
  -moz-box-shadow: 0px 0px 100px 5px rgba(255, 0, 100, 0.4);
  -webkit-box-shadow: 0px 0px 100px 5px rgba(255, 0, 100, 0.4);
  box-shadow: 0px 0px 100px 5px rgba(255, 0, 100, 0.4);
}
</style>
