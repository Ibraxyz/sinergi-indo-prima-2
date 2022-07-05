<template>
  <div class="threed-wrapper">
    <!-- the 3d canvas -->
    <div class="threed-content">
      <div
        :class="[activeIndex === index ? 'threedbox threedbox-active' : 'threedbox']"
        v-for="(i, index) of Imgs"
        @click="changePicture(i, index)"
      >
        <img :src="i" atl="" />
      </div>
    </div>
  </div>
  <div class="threed-displayer">
    <div style="position: relative; width: 100%; height: 100%">
      <img :src="selectedImg" alt="" />
      <div class="img-cover inShadow" />
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Satpam from "../assets/gambar1.png";
import CleaningService from "../assets/cleaningservice.png";
import Cs from "../assets/cs.png";
import KaryawanPerkantoran from "../assets/karyawan-perkantoran.png";
import Sales from "../assets/sales.png";
import Pp from "../assets/pp3.png";

const Imgs = [CleaningService, Pp, Satpam, Cs, KaryawanPerkantoran, Sales, Pp, Satpam];

const emit = defineEmits(["changeBackground"]);

const selectedImg = ref(KaryawanPerkantoran);
const activeIndex = ref(4);

function changePicture(i, index) {
  selectedImg.value = i;
  activeIndex.value = index;
  emit("changeBackground", i);
}
</script>

<style scoped>
.threed-wrapper {
  position: absolute;
  width: 60%;
  height: 25%;
  perspective: 600px;
  bottom: 12%;
  right: 0;
  font-size: 0px; /** for removing white space on vertical axis of the inline block divs */
  z-index: 3;
}
.threed-content {
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transform: rotateX(0deg);
  -webkit-animation: images-entry-rotate 1s linear alternate both;
  animation: images-entry-rotate 1s linear alternate both;
}

.threed-displayer {
  position: absolute;
  width: 52%;
  height: 30%;
  bottom: 30%;
  right: 4%;
  overflow: hidden;
  z-index: 3;
  -moz-box-shadow: 0px 0px 300px 100px rgba(255, 0, 100, 0.4);
  -webkit-box-shadow: 0px 0px 300px 100px rgba(255, 0, 100, 0.4);
  box-shadow: 0px 0px 300px 100px rgba(255, 0, 100, 0.4);
  border: 1px solid rgba(255, 0, 100, 1);
}

.img-cover {
  position: absolute;
  box-sizing: border-box;
  top: 0px;
  left: 0px;
  width: 100%;
  height: 100%;
}

.threed-displayer img {
  width: 100%;
  height: auto;
}

.inShadow {
  -moz-box-shadow: inset 0 0 100px rgba(50, 0, 125, 0.9);
  -webkit-box-shadow: inset 0 0 100px rgba(50, 0, 125, 0.9);
  box-shadow: inset 0 0 100px rgba(50, 0, 100, 0.9);
}

@keyframes images-entry-rotate {
  0% {
    transform: rotateX(0deg);
  }
  100% {
    transform: rotateX(60deg);
  }
}

@-webkit-keyframes images-entry-rotate {
  0% {
    transform: rotateX(0deg);
  }
  100% {
    transform: rotateX(60deg);
  }
}

.threedbox {
  box-sizing: border-box;
  display: inline-block;
  width: 25%;
  height: 50%;
  overflow: hidden;
  position: relative;
  border: 1px solid rgba(255, 0, 100, 1);
}

.threedbox:hover {
  border: 10px solid rgba(255, 0, 100, 1);
  cursor: pointer;
}

.threedbox-active {
  border: 10px solid rgba(255, 0, 100, 1);
  cursor: pointer;
}

.threedbox img {
  width: 180%;
  height: auto;
  opacity: 0.3;
}

.threedbox img:hover {
  opacity: 1;
}
</style>
