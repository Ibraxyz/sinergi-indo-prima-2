<template>
  <div style="position: relative">
    <!-- some decorated divs -->

    <!-- upper decor -->

    <!-- shadow for triangle div -->
    <div
      style="
        position: absolute;
        top: 6px;
        left: 0px;
        width: 100%;
        height: 98%;
        z-index: 1000;
      "
    >
      <!--
      this div is used to make a shadow for triangle div.. 
      if we apply shadow directly to a div, it will resulting incorrect effect,
      because of  small rectangle at the top left of triangle div,
      so we design this div for creating a correct effect for the triangle div
      
      planned div : 

                        --------
                        |      |
                        |      |
                        |  div |
                        |      |
                        |      |
      ------------------       | 
      |                 |      |
      |          div    |      |            
      |                 |      |
      -------------------------- 

      and after these two divs are created, then, we apply box-shadow to both of those two divs.
      -->
      <div style="position: relative; width: 100%; height: 100%">
        <div
          style="
            height: 0px;
            display: inline-block;
            width: 99%;
            box-sizing: border-box;
            box-shadow: 5px 5px 12px rgba(0, 0, 0, 0.4);
          "
        ></div>
        <div
          style="
            display: inline-block;
            width: 1%;
            height: 100%;
            box-sizing: border-box;
            box-shadow: 5px 5px 12px rgba(0, 0, 0, 0.4);
          "
        ></div>
      </div>
    </div>

    <!--triangle cornered div that display image -->
    <div style="width: auto; height: 100%; overflow: hidden; position: relative">
      <!-- the top left triangle for cut off the top left corner of the image's div -->
      <DivTriangle :bgColor="props.triangleColor" />

      <!-- from top gradient-->
      <div
        style="
          background: #000000;
          background: -webkit-linear-gradient(to bottom, #000000, rgba(29, 67, 80, 0.1));
          background: linear-gradient(to bottom, #000000, rgba(29, 67, 80, 0.1));
          z-index: 5;

          position: absolute;
          top: 0px;
          left: 0px;
          width: 100%;
          height: 30%;
          opacity: 0.8;
        "
      ></div>

      <!-- sip mini logo -->
      <img
        src="../assets/sip-transparent.png"
        style="
          width: 48px;
          height: auto;
          position: absolute;
          top: 40px;
          left: 60px;
          z-index: 10;
        "
      />

      <img src="../assets/gambar1.png" alt="" style="width: auto; height: 100%" />
    </div>
    <!-- end of triangle cornered div -->
  </div>
</template>

<script setup>
import { ref } from "vue";
import DivTriangle from "./DivTriangle.vue";
const props = defineProps(["img", "triangleColor"]);
const imgUrl = ref(props.img);
</script>

<style scoped></style>
