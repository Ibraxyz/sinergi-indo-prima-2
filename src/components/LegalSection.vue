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
    <!-- wrapper for full screen image viewer (documents) -->
    <FullscreenDoc
      :isVisible="isFullScreenViewerVisible"
      :images="Legals"
      :activeIndex="activeLegal"
      @close-event="isFullScreenViewerVisible = false"
      @change-event="changePic($event)"
    />
    <Container style="transform: skewY(11deg)">
      <div class="col5" style="position: relative">
        <!-- wrapper for info display -->
        <div
          style="
            position: absolute;
            width: 100%;
            z-index: 4;
            color: #ffffff;
            bottom: 60px;
            left: 0px;
            text-align: center;
          "
        >
          <Typography variant="p" mode="light">
            {{ Legals[activeLegal].name }} - {{ activeLegal + 1 }}/{{
              Legals.length
            }}</Typography
          >
        </div>
        <!-- wrapper for left nav buttons -->
        <div
          style="
            width: 64px;
            height: 100%;
            z-index: 5;
            position: absolute;
            top: 0px;
            left: 0px;
            display: flex;
            align-items: center;
            justify-content: flex-end;
          "
        >
          <!-- nav buttons -->
          <BaseTriangle
            style="cursor: pointer"
            position="right"
            @click="shiftLegal('left')"
          />
        </div>
        <!-- wrapper for right nav buttons -->
        <div
          style="
            width: 64px;
            height: 100%;
            z-index: 5;
            position: absolute;
            top: 0px;
            right: 0px;
            display: flex;
            align-items: center;
          "
        >
          <!-- nav buttons -->
          <BaseTriangle
            style="cursor: pointer"
            position="left"
            @click="shiftLegal('right')"
          />
        </div>

        <!-- 3d projection -->
        <div style="position: relative; height: 400px; perspective: 600px; z-index: 3">
          <div
            class="rotatedDiv"
            style="transform-style: preserve-3d; position: relative"
          >
            <LegalDocument :info="Legals[activeLegal]" />
            <!-- wrapper for search icon button -->
            <div
              class="searchIconWrapper"
              style="
                position: absolute;
                top: 0px;
                left: 0px;
                width: 100%;
                height: 100%;
                display: flex;
                z-index: 4;
                justify-content: center;
              "
            >
              <!-- search icon button-->
              <div
                style="width: 64px; height: 64px; position: relative; top: 26%"
                @click="isFullScreenViewerVisible = true"
              >
                <img :src="SearchIcon" alt="" style="width: 100%; height: auto" />
              </div>
            </div>
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
import { ref } from "vue";
import Container from "./Container.vue";
import Typography from "./Typography.vue";
import LegalDocument from "./LegalDocument.vue";
import SearchIcon from "../assets/icons8-search-100.png/";
import BaseTriangle from "./BaseTriangle.vue";
import FullscreenDoc from "./FullscreenDoc.vue";
import Legal1 from "../assets/legal1.png/";
import Legal2 from "../assets/legal2.png/";
import Legal3 from "../assets/legal3.png/";
import Legal4 from "../assets/legal4.png/";
import Legal5 from "../assets/legal5.png/";
import Legal6 from "../assets/legal6.png/";
import Legal7 from "../assets/legal7.png/";
import Legal8 from "../assets/legal8.png/";
import Legal9 from "../assets/legal9.png/";
import Legal10 from "../assets/legal10.png/";
import Legal11 from "../assets/legal11.png/";
import Legal12 from "../assets/legal12.png/";
import Legal13 from "../assets/legal13.png/";
import Legal14 from "../assets/legal14.png/";
import Legal15 from "../assets/legal15.png/";
import Legal16 from "../assets/legal16.png/";

const Legals = [
  {
    name:
      "Akta Pendirian Perusahaan Nomor : 08,Tanggal 08 Agustus 2017, Notaris : Lila Meutia, SH, MkN",
    img: Legal1,
  },
  {
    name: "Pengesahan Akta Pendirian Nomor : AHU-0034093.AH.01.01.Tahun 2017",
    img: Legal2,
  },
  {
    name: "Surat Domisili Perusahaan Nomor : 503/1151",
    img: Legal3,
  },
  {
    name: "OSS Izin Usaha Perdagangan",
    img: Legal4,
  },
  {
    name: "Dokumen 05",
    img: Legal5,
  },
  {
    name: "Dokumen 06",
    img: Legal6,
  },
  {
    name: "Dokumen 07",
    img: Legal7,
  },
  {
    name: "Dokumen 08",
    img: Legal8,
  },
  {
    name: "Dokumen 09",
    img: Legal9,
  },
  {
    name: "Dokumen 10",
    img: Legal10,
  },
  {
    name: "Dokumen 11",
    img: Legal11,
  },
  {
    name: "Surat Keterangan Terdaftar Pajak (SKT) Nomor : S-5980KT/WPJ.01/KP.0503/2017",
    img: Legal12,
  },
  {
    name: "Sertifikat BPJS Kesehatan Nomor : 00388526",
    img: Legal13,
  },
  {
    name: "Sertifikat BPJS Ketenagakerjaan Nomor : 170000000244567",
    img: Legal14,
  },
  {
    name: "NPWP : No. 82.653.691.4-113.000",
    img: Legal15,
  },
  {
    name: "Dokumen 16",
    img: Legal16,
  },
];

const activeLegal = ref(0);
const isFullScreenViewerVisible = ref(false);

function shiftLegal(dir) {
  switch (dir) {
    case "left":
      if (activeLegal.value > 0) {
        activeLegal.value--;
      }
      break;
    case "right":
      if (activeLegal.value < Legals.length - 1) {
        activeLegal.value++;
      }
      break;
    default:
      break;
  }
}

function changePic(e) {
  //alert("from parent" + e);
  activeLegal.value = e;
  /**
Akta Pendirian Perusahaan Nomor : 08,Tanggal 08 Agustus 2017, Notaris : Lila Meutia, SH, MkN;
Pengesahan Akta Pendirian Nomor : AHU-0034093.AH.01.01.Tahun 2017;
Surat Domisili Perusahaan Nomor : 503/1151;
OSS Nomor Induk Berusaha (NIB) : No. 8120012241154;
OSS Izin Usaha Perdagangan;
OSS badan Usaha Jasa Pengamanan;
OSS Izin Usaha Perusahaan Penyedia Jasa Pekerja/Buruh;
Surat Izin Operasional dari Polri sebagai badan usaha jasa penyedia tenaga pengamanan;
NPWP : No. 82.653.691.4-113.000;
Surat Keterangan Terdaftar Pajak (SKT) Nomor : S-5980KT/WPJ.01/KP.0503/2017;
Surat Pengukuhan Pengusaha Kena Pajak (SPPKP) Nomor : S-363PKP/WPJ.01/KP.0503/2017;
Sertifikat BPJS Ketenagakerjaan Nomor : 170000000244567;
Sertifikat BPJS Kesehatan Nomor : 00388526;
Sertifikat Asosiasi Badan usaha jasa pengamanan indonesia (ABUJPI) Nomor : 02038/17-10-2017;
   */
}
</script>

<style scoped>
.wrapper {
  box-sizing: border-box;
  padding-top: 80px;
  padding-left: 15px;
  padding-right: 15px;
  padding-bottom: 15px;
  background-color: #020b4a;
  position: relative;
  transform: skewY(-11deg);
  margin-top: 0px;
  padding-top: 200px;
  padding-bottom: 200px;
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
.searchIconWrapper {
  opacity: 0;
}
.searchIconWrapper:hover {
  opacity: 1;
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
