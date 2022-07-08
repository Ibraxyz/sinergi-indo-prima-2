<template>
  <!-- Hero -->
  <HeroVer2>
    <template #desktopmenu>
      <nav style="position: absolute; top: 0px; left: 0px; z-index: 3; width: 100%">
        <Container>
          <ul>
            <li>
              <img
                src="./assets/sip-transparent.png"
                alt=""
                style="width: 64px; height: auto"
              />
            </li>
            <li>
              <TopMenuItem text="Home" />
            </li>
            <li>
              <TopMenuItem text="About" />
            </li>
            <li>
              <TopMenuItem text="Service" />
            </li>
            <li>
              <TopMenuItem text="Facilities" />
            </li>
            <li>
              <TopMenuItem text="Legal" />
            </li>
            <li>
              <TopMenuItem text="Contact" />
            </li>
          </ul>
        </Container>
      </nav>
    </template>
  </HeroVer2>
  <!--<Hero>
    
    <template v-slot:background>
      <div
        :style="{
          opacity: 0.0,
          width: '100%',
          height: '100%',
        }"
      ></div>
    </template>
      <template #content>
      <div class="temp">
        <nav>
          <Container>
            <ul>
              <li>
                <img
                  src="./assets/sip-transparent.png"
                  alt=""
                  style="width: 80px; height: auto"
                />
              </li>
              <li>
                <TopMenuItem text="Home" />
              </li>
              <li>
                <TopMenuItem text="About" />
              </li>
              <li>
                <TopMenuItem text="Service" />
              </li>
              <li>
                <TopMenuItem text="Facilities" />
              </li>
              <li>
                <TopMenuItem text="Legal" />
              </li>
              <li>
                <TopMenuItem text="Contact" />
              </li>
            </ul>
          </Container>
        </nav>

        <div class="content">
          <Container>
            <div
              style="
                box-sizing: border-box;
                padding-top: 20px;
                position: relative;
                background: black;
              "
            >
              <div class="col-4" style="background: red">
                <Typography variant="h1" mode="light"
                  >The Most Reliable Service Provider</Typography
                >
                <Typography variant="p" mode="light">
                  Perusahaan penyedia jasa prima, handal, baik dan profesional serta
                  memiliki standard nasional dan terpercaya.
                </Typography>
              </div>
              <div class="col-6" style="overflow: hidden; background: red">
                  <img
                  src="./assets/gambar1.png"
                  alt=""
                  style="
                    width: auto;
                    height: 100%;
                    margin-top: 20p;
                    position: relative;
                    z-index: 20x;
                  "
                /> 
              </div>
              <div style="text-align: center">
              </div>
              <div style="text-align: center; margin-top: 50px">
                <img
                  src="./assets/images/arrow_downward_24px.svg"
                  alt=""
                  class="shake-vertical"
                  style="position: relative"
                /> 
              </div>
            </div>
          </Container>
        </div>
      </div>
    </template> 
    <template #dynamic>
      <div
        style="
          position: relative;
          width: 60%;
          height: 60%;
          margin-left: auto;
          margin-right: auto;
          margin-top: 230px;
          perspective: 600px;
        "
      >
        <div class="dyn-images-entry">
          <div
            v-for="i of [
              CleaningService,
              Pp,
              Satpam,
              Cs,
              KaryawanPerkantoran,
              Sales,
              Pp,
              Satpam,
              CleaningService,
              Cs,
              KaryawanPerkantoran,
              CleaningService,
              Pp,
              Satpam,
              Cs,
              KaryawanPerkantoran,
            ]"
            class="threedbox"
          >
            <div class="threedimg">
              <img :src="i" alt="" />
            </div>
          </div>
        </div>
      </div>
    </template>
  </Hero> -->

  <!-- services list -->
  <div
    style="
      position: relative;
      transform: skewY(-11deg);
      background-color: #020b4a;
      z-index: 100;
      padding-top: 90px;
      padding-bottom: 90px;
    "
  >
    <!-- decor -->
    <div
      style="
        position: absolute;
        top: -250px;
        left: 0px;
        background-color: #020b4a;
        width: 100%;
        height: 300px;
      "
    >
      <div style="position: relative; width: 100%; height: 100%">
        <DecorLineBg
          style="transform: skewY(11deg); position: absolute"
          to="bottom"
          top="100px"
          left="66%"
          right="50%"
          height="100%"
          width="10px"
        />
        <DecorLineBg
          style="transform: skewY(11deg); position: absolute"
          to="bottom"
          top="300px"
          left="66%"
          right="50%"
          height="100%"
          width="10px"
        />
        <DecorLineBg
          style="transform: skewY(11deg); position: absolute"
          to="bottom"
          top="2630px"
          left="30%"
          right="50%"
          height="400px"
          width="10px"
        />
        <!-- decor line -->
        <div
          class="first-decor"
          style="
            position: absolute;
            top: 0px;
            left: 0px;
            background-image: linear-gradient(to right, rgba(255, 0, 100, 1), red);
            height: 7px;
          "
        ></div>
      </div>
    </div>
    <Section1 style="transform: skewY(11deg)">
      <ServiceSection />
    </Section1>
  </div>

  <!-- training dan edukasi -->
  <div style=""><TrainingAndEducation /></div>

  <!-- facilities -->
  <FacilitiesSection />

  <!-- our clients -->

  <!-- legals -->
  <LegalSection />
</template>

<script setup>
import "./assets/base.css";
import Hero from "./components/Hero.vue";
import { ref } from "vue";
import Button from "./components/Button.vue";
import Bg from "./assets/tile_background.png";
import TopMenuItem from "./components/TopMenuItem.vue";
import Section1 from "./components/Section1.vue";
import ServiceSection from "./components/ServiceSection.vue";
import FacilitiesSection from "./components/FacilitiesSection.vue";
import Container from "./components/Container.vue";
import Typography from "./components/Typography.vue";
import ThreedBox from "./components/ThreedBox.vue";
import HeroImageGroup from "./components/HeroImageGroup.vue";
import ContactSection from "./components/ContactSection.vue";
import TrainingAndEducation from "./components/TrainingAndEducation.vue";
import DecorLineBg from "./components/DecorLineBg.vue";

import Satpam from "./assets/gambar1.png";
import CleaningService from "./assets/cleaningservice.png";
import Cs from "./assets/cs.png";
import KaryawanPerkantoran from "./assets/karyawan-perkantoran.png";
import Sales from "./assets/sales.png";
import Pp from "./assets/pp3.png";

import HeroVer2 from "./components/HeroVer2.vue";

import LegalSection from "./components/LegalSection.vue";

const images = ref(["ar1.jpg", "sip1.png", "sip2.png"]);
const bgImg = ref(Bg);
const bottomDivIndex = ref(-1);

function showBottomDiv(num) {
  bottomDivIndex.value = num;
}

function hideBottomDiv(num) {
  bottomDivIndex.value = 0;
}
</script>

<style scoped>
.borderBottomRed {
  border-bottom: 3px solid red;
  margin-top: 3px;
}

ul {
  display: flex;
  justify-content: right;
  align-items: center;
  margin: 0px;
  box-sizing: border-box;
  padding: 10px;
}

ul li {
  padding-top: 15px;
  margin: 10px 20px 10px 0px;
  /** text-transform: uppercase; **/
  list-style-type: none;
  cursor: pointer;
}

.col-6 {
  width: 60%;
  box-sizing: border-box;
  padding: 15px;
  display: inline-block;
  vertical-align: middle;
}

.threedbox {
  box-sizing: border-box;
  display: inline-block;
  width: 25%;
  height: 25%;
  padding: 0px;
}

.dyn-images-entry {
  width: 100%;
  height: 100%;
  transform-style: preserve-3d;
  transform: rotateX(0deg);
  -webkit-animation: images-entry-rotate 1s linear alternate both;
  animation: images-entry-rotate 1s linear alternate both;
}

@-webkit-keyframes images-entry-rotate {
  0% {
    transform: rotateX(0deg);
  }
  100% {
    transform: rotateX(45deg);
  }
}

@keyframes images-entry-scale {
  0% {
    width: 0%;
    height: 0%;
  }
  50% {
    width: 52%;
    height: 0%;
  }
  100% {
    width: 52%;
    height: 30%;
  }
}

@-webkit-keyframes images-entry-scale {
  0% {
    width: 0%;
    height: 0%;
  }
  50% {
    width: 52%;
    height: 0%;
  }
  100% {
    width: 52%;
    height: 30%;
  }
}

.col-4 {
  width: 40%;
  box-sizing: border-box;
  padding: 15px;
  display: inline-block;
  vertical-align: middle;
}

.threedimg {
  width: 100%;
  height: 100%;
  overflow: hidden;
  box-sizing: border-box;
  position: relative;
}

.threedimg img {
  width: 100%;
  height: auto;
  opacity: 0.2;
}

.threedimg img:hover {
  width: 100%;
  height: auto;
  opacity: 1;
  cursor: pointer;
}

.threedimg:hover {
  border: 5px solid red;
}

.big-hero-img {
  width: auto;
  height: 500px;
}

.small-hero-img {
  display: none;
}

.small-hero-img div {
  display: inline-block;
  box-sizing: border-box;
  width: 50%;
  overflow: hidden;
  height: 250px;
}

ul li:first-child {
  margin-right: auto;
}

ul li:last-child {
  margin-right: 0px;
}

/* ----------------------------------------------
 * Generated by Animista on 2022-5-24 16:42:49
 * Licensed under FreeBSD License.
 * See http://animista.net/license for more info.
 * w: http://animista.net, t: @cssanimista
 * ---------------------------------------------- */

/**
 * ----------------------------------------
 * animation shake-vertical
 * ----------------------------------------
 */

.shake-vertical {
  -webkit-animation: shake-vertical 8s cubic-bezier(0.455, 0.03, 0.515, 0.955) infinite
    both;
  animation: shake-vertical 8s cubic-bezier(0.455, 0.03, 0.515, 0.955) infinite both;
}

@-webkit-keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }

  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-8px);
    transform: translateY(-8px);
  }

  20%,
  40%,
  60% {
    -webkit-transform: translateY(8px);
    transform: translateY(8px);
  }

  80% {
    -webkit-transform: translateY(6.4px);
    transform: translateY(6.4px);
  }

  90% {
    -webkit-transform: translateY(-6.4px);
    transform: translateY(-6.4px);
  }
}

@keyframes shake-vertical {
  0%,
  100% {
    -webkit-transform: translateY(0);
    transform: translateY(0);
  }

  10%,
  30%,
  50%,
  70% {
    -webkit-transform: translateY(-8px);
    transform: translateY(-8px);
  }

  20%,
  40%,
  60% {
    -webkit-transform: translateY(8px);
    transform: translateY(8px);
  }

  80% {
    -webkit-transform: translateY(6.4px);
    transform: translateY(6.4px);
  }

  90% {
    -webkit-transform: translateY(-6.4px);
    transform: translateY(-6.4px);
  }
}

@media only screen and (max-width: 768px) {
  .col-4,
  .col-6 {
    width: 100%;
  }

  ul {
    display: none;
  }

  .big-hero-img {
    display: none;
  }

  .small-hero-img {
    display: block;
  }
}

/** very small device screen **/
@media only screen and (max-width: 400px) {
  .small-hero-img div:first-child img {
    top: 20px;
  }
}

.first-decor {
  width: 0%;
  -webkit-animation: first-decor-anim 1s linear alternate both;
  animation: first-decor-anim 1s linear alternate both;
}

@keyframes first-decor-anim {
  0% {
    width: 0%;
  }
  100% {
    width: 100%;
  }
}

@-webkit-keyframes first-decor-anim {
  0% {
    width: 0%;
  }
  100% {
    width: 100%;
  }
}
</style>
