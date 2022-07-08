<template>
  <div class="t-wrapper">
    <!-- decor line -->
    <div
      style="
        position: absolute;
        top: 0px;
        left: 0px;
        background-image: linear-gradient(to right, rgba(255, 0, 100, 1), red);
        height: 7px;
        width: 100%;
      "
    ></div>
    <Container style="transform: skewY(11deg); padding-top: 200px; padding-bottom: 200px">
      <!-- background -->
      <div style="position: relative">
        <div class="col5"></div>
        <div class="col5">
          <div style="display: inline-block">
            <Typography variant="h2" mode="light">Training dan Edukasi</Typography>
            <div class="borderBottomRed"></div>
          </div>
          <Typography variant="p" mode="light">
            Dengan mengikuti pelatihan intensif, para calon tenaga kerja akan mendapatkan
            pengetahuan dan keterampilan yang memadai serta mendukung performa mereka
            dalam bekerja. training dan edukasi menjadi hal pokok yang harus dimiliki
            setiap tenaga kerja, guna menciptakan tenaga kerja yang profesional.
          </Typography>
        </div>
      </div>
    </Container>
  </div>
</template>

<script setup>
import Container from "./Container.vue";
import Typography from "./Typography.vue";
</script>

<style scoped>
.t-wrapper {
  /** #02072f */
  position: relative;
  background-color: #020b4a;
  box-sizing: border-box;
  color: #ffffff;
  transform: skewY(-11deg);
}
.borderBottomRed {
  width: 100%;
  border-bottom: 3px solid red;
  margin-top: 3px;
}
.col5 {
  display: inline-block;
  padding: 15px;
  box-sizing: border-box;
  width: 50%;
  vertical-align: top;
}
@media only screen and (max-width: 768px) {
  .col5 {
    width: 100%;
  }
}
</style>
