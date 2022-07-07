<template>
  <div class="wrapper">
    <Container noPadding>
      <div class="col5">
        <!-- 3d projection -->
        <div style="position: relative; height: 400px; perspective: 600px">
          <div class="rotatedDiv" style="transform-style: preserve-3d">
            <LegalDocument />
          </div>
        </div>
      </div>
      <div class="col5">
        <div style="display: inline-block">
          <Typography variant="h2" mode="light">Legalitas</Typography>
          <div class="borderBottomRed"></div>
        </div>
        <Typography variant="p" mode="light">
          Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
          standard nasional dan terpercaya.</Typography
        >
        <Typography variant="span" mode="light">Pelajari lebih lanjut</Typography>
      </div>
    </Container>
  </div>
</template>

<script setup>
import Container from "./Container.vue";
import Typography from "./Typography.vue";
import LegalDocument from "./LegalDocument.vue";
</script>

<style scoped>
.wrapper {
  box-sizing: border-box;
  padding-top: 80px;
  padding-left: 15px;
  padding-right: 15px;
  padding-bottom: 15px;
  background-color: #020b4a;
}
h1 {
  margin: 0px;
  color: #ffffff;
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
.rotatedDiv {
  transform: rotateY(30deg);
  -webkit-animation: images-entry-rotate-default 1s linear alternate both;
  animation: images-entry-rotate-default 1s linear alternate both;
}

.rotatedDiv:hover {
  transform: rotateY(0deg);
  -webkit-animation: images-entry-rotate 1s linear alternate both;
  animation: images-entry-rotate 1s linear alternate both;
  cursor: pointer;
}
@keyframes images-entry-rotate {
  0% {
    transform: rotateY(30deg);
  }
  100% {
    transform: rotateY(0deg);
  }
}

@-webkit-keyframes images-entry-rotate {
  0% {
    transform: rotateY(30deg);
  }
  100% {
    transform: rotateY(0deg);
  }
}

@keyframes images-entry-rotate-default {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(30deg);
  }
}

@-webkit-keyframes images-entry-rotate-default {
  0% {
    transform: rotateY(0deg);
  }
  100% {
    transform: rotateY(30deg);
  }
}
@media only screen and (max-width: 768px) {
  .col5 {
    width: 100%;
  }
}
</style>
