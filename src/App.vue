<template>
  <Hero>
    <template v-slot:background>
      <AnimatedBackground :images="images" />
    </template>
    <template #content>
      <div class="temp">
        <nav>
          <div class="container" >
            <ul>
              <li >Logo</li>
              <li>Home</li>
              <li>About</li>
              <li>Service</li>
            </ul>
          </div>
        </nav>
        <div class="content">
          <div class="container">
            <div style="box-sizing: border-box; padding-top: 200px">
              <h1 style="font-size: 100px; margin: 0px">Grow Together.</h1>
              <p style="max-width: 650px; opacity: 0.8; font-size: 24px">
                It is a long established fact that a reader will be distracted by the
                readable content of a page when looking at its layout. The point of using
                Lorem Ipsum is that it has a more-or-less normal distribution of letters,
                as opposed to using 'Content here, content here', making it look like
                readable English.
              </p>
            </div>
          </div>
        </div>
      </div>
    </template>
  </Hero>
    <Hero>
    <template v-slot:background>
      <AnimatedBackground :images="images" />
    </template>
    <template #content>
      <div class="temp">
        <nav>
          <div class="container" >
            <ul>
              <li >Logo</li>
              <li>Home</li>
              <li>About</li>
              <li>Service</li>
            </ul>
          </div>
        </nav>
        <div class="content">
          <div class="container">
            <div style="box-sizing: border-box; padding-top: 200px">
              <h1 style="font-size: 100px; margin: 0px">Grow Together.</h1>
              <p style="max-width: 650px; opacity: 0.8; font-size: 24px">
                It is a long established fact that a reader will be distracted by the
                readable content of a page when looking at its layout. The point of using
                Lorem Ipsum is that it has a more-or-less normal distribution of letters,
                as opposed to using 'Content here, content here', making it look like
                readable English.
              </p>
            </div>
          </div>
        </div>
      </div>
    </template>
  </Hero>
</template>

<script setup>
import "./assets/base.css";
import AnimatedBackground from "./components/AnimatedBackground.vue";
import Hero from "./components/Hero.vue";
import { ref } from "vue";

const images = ref(["bg1.png", "bg2.png", "bg3.png"]);
</script>

<style scoped>
.temp {
  color: #ffffff;
}

ul {
  display: flex;
  justify-content: right;
  margin: 0px;
  box-sizing: border-box;
  padding: 10px;
}

ul li {
  padding-top:10px;
  margin: 10px 20px 10px 0px;
  text-transform: uppercase;
  list-style-type: none;
  cursor: pointer;
}

ul li:first-child {
  margin-right: auto;
}

ul li:last-child{
  margin-right:0px;
}

.content {
}

.container {
  box-sizing: border-box;
  max-width: 1110px;
  margin: auto;
}
</style>
