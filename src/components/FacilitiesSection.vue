<template>
  <div class="wrapper">
    <!-- decor line -->
    <div
      style="
        position: absolute;
        top: 0px;
        left: 0px;
        background-image: linear-gradient(to right, rgba(255, 0, 100, 1), blue);
        height: 1px;
        width: 100%;
      "
    ></div>
    <Container
      style="transform: skewY(11deg); padding-top: 200px; padding-bottom: 200px"
    >
      <div class="col5">
        <div style="display: inline-block">
          <Typography variant="h2" mode="light">Facilities</Typography>
          <div class="borderBottomRed"></div>
        </div>
        <Typography variant="p" mode="light">
          Fasilitas kantor memiliki dampak yang baik dalam mendukung dan
          meningkatkan kinerja karyawan, tentunya kami persiapkan dengan lengkap
          sesuai dengan kebutuhan & perkembangan serta mendengarkan dan menerima
          segala bentuk kritik dan saran yang bersifat membangun dengan harapan
          agar PT. Sinergi Indo Prima menjadi partner bekerja sama yang
          fleksible dan komunikatif.
        </Typography>
      </div>
      <div class="col5">
        <ImageNavigator />
      </div>
    </Container>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Typography from "./Typography.vue";
import Container from "./Container.vue";
import ImageNavigator from "./ImageNavigator.vue";

/**
<div style="display: inline-block">
<Typography variant="h2" mode="light">Facilities</Typography>
<div class="borderBottomRed"></div>
</div>
 */
</script>

<style scoped>
.wrapper {
  position: relative;
  width: 100%;
  transform: skewY(-11deg);
  background: rgba(2, 11, 74, 0.9); /* fallback for old browsers */
  background: -webkit-linear-gradient(
    to right,
    #020b4a,
    rgba(2, 11, 74, 0.9)
  ); /* Chrome 10-25, Safari 5.1-6 */
  background: linear-gradient(
    to right,
    #020b4a,
    rgba(2, 11, 74, 0.9)
  ); /* W3C, IE 10+/ Edge, Firefox 16+, Chrome 26+, Opera 12+, Safari 7+ */
}
.borderBottomRed {
  width: 100%;
  border-bottom: 3px solid red;
  margin-top: 3px;
}
/** reddish gradient
      background: #c94b4b;
      background: -webkit-linear-gradient(to right, #4b134f, #c94b4b);
      background: linear-gradient(to right, #4b134f, #c94b4b); */

/** blueish background
      background: #0f0c29;  
background: -webkit-linear-gradient(to right, #24243e, #302b63, #0f0c29);  
background: linear-gradient(to right, #24243e, #302b63, #0f0c29); 

      */
</style>
