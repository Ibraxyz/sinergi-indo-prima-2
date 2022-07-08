<template>
  <!-- image navigator -->
  <div
    style="
      width: 100%;
      height: 300px;
      overflow: hidden;
      text-align: center;
      background: #020b4a;
    "
    class="displayImg"
  >
    <img :src="selectedPhoto" alt="" style="width: auto; height: 300px" />
  </div>
  <div
    style="
      margin-top: 10px;
      display: flex;
      align-items: center;
      justify-content: space-between;
      width: 100%;
    "
  >
    <div
      style="
        border-top: 1px solid rgba(255, 0, 100, 1);
        border-left: 1px solid rgba(255, 0, 100, 1);
        border-bottom: 1px solid rgba(255, 0, 100, 1);
        box-sizing: border-box;
        padding: 5px;
        cursor: pointer;
      "
      @click="shiftPhoto('left')"
    >
      <BaseTriangle position="right" style="position: relative; left: -30%" />
    </div>
    <div
      style="
        box-sizing: border-box;
        overflow-x: scroll;
        flex: 1;
        border: 1px solid rgba(255, 0, 100, 1);
        height: 52px;
        white-space: nowrap;
      "
    >
      <img
        v-for="i of Imgs"
        class="small-thumb"
        alt=""
        :src="i"
        @click="changePhoto(i)"
      />
    </div>
    <div
      style="
        border-top: 1px solid rgba(255, 0, 100, 1);
        border-right: 1px solid rgba(255, 0, 100, 1);
        border-bottom: 1px solid rgba(255, 0, 100, 1);
        box-sizing: border-box;
        padding: 5px;
        cursor: pointer;
      "
      @click="shiftPhoto('right')"
    >
      <BaseTriangle position="left" style="position: relative; right: -30%" />
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
import BaseTriangle from "./BaseTriangle.vue";

const Imgs = [Satpam, Cs, CleaningService, KaryawanPerkantoran, Sales, Pp];
const selectedPhoto = ref(Satpam);

function changePhoto(p) {
  selectedPhoto.value = p;
}

function shiftPhoto(direction) {
  let currentIndex = Imgs.indexOf(selectedPhoto.value);
  switch (direction) {
    case "left":
      if (currentIndex == 0) {
      } else {
        currentIndex--;
        changePhoto(Imgs[currentIndex]);
      }
      break;
    case "right":
      if (currentIndex == Imgs.length - 1) {
      } else {
        currentIndex++;
        changePhoto(Imgs[currentIndex]);
      }
      break;

    default:
      break;
  }
}
</script>

<style scoped>
.displayImg {
  border: 1px solid rgba(255, 0, 100, 1);
  -moz-box-shadow: 0px 0px 100px 100px rgba(255, 0, 100, 0.2);
  -webkit-box-shadow: 0px 0px 100px 100px rgba(255, 0, 100, 0.2);
  box-shadow: 0px 0px 100px 100px rgba(255, 0, 100, 0.2);
}
.small-thumb {
  height: 52px;
  width: auto;
  opacity: 0.5;
  cursor: pointer;
  box-sizing: border-box;
}
.small-thumb:hover {
  opacity: 1;
}
</style>
