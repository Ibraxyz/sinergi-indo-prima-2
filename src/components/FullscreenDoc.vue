<template>
  <div class="wrapperz">
    <!-- wrapper for image navigator and image displayer -->
    <div style="width: 100%; height: 100%; top: 0px; left: 0px; position: absolute">
      <!-- image navigator -->
      <div
        style="
          display: inline-block;
          width: 20%;
          height: 100%;
          background-color: #000000;
          box-sizing: border-box;
          box-shadow: 30px 30px 12px solid rgba(0, 0, 0, 0.4);
        "
      ></div>

      <!-- image displayer -->
      <div
        style="
          display: inline-block;
          width: 80%;
          height: 100%;
          box-sizing: border-box;
          overflow: scroll;
        "
      ></div>
    </div>
    <!-- wrapper for x button wrapper -->
    <div
      style="
        position: absolute;
        width: 64px;
        height: 64px;
        top: 0px;
        right: 0px;
        z-index: 102;
      "
    >
      <!-- wrapper for (X) button -->
      <div style="position: relative; cursor: pointer; width: 64px; height: 64px">
        <!-- the (x) button it self -->
        <div
          style="
            position: absolute;
            top: 50%;
            margin-top: -5px;
            border: 3px solid #ffffff;
            width: 80%;
            box-sizing: border-box;
            z-index: 103;
            transform: rotate(-45deg);
          "
        ></div>
        <div
          style="
            position: absolute;
            top: 50%;
            margin-top: -5px;
            border: 3px solid #ffffff;
            width: 80%;
            box-sizing: border-box;
            z-index: 104;
            transform: rotate(45deg);
          "
        ></div>
      </div>
    </div>
  </div>
</template>

<script setup></script>

<style scoped>
.wrapperz {
  position: fixed;
  top: 0px;
  left: 0px;
  background-color: #242424;
  width: 100%;
  height: 100%;
  z-index: 100;
}
</style>
