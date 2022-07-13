<template>
  <div class="contact-wrapper" style="position: relative">
    <!-- team artwork decor -->
    <img :src="Building" class="team" alt="" />

    <!-- building artwork decor 
    <a href='https://www.freepik.com/vectors/metropolis'>Metropolis vector created by upklyak - www.freepik.com</a>
    -->
    <div class="decor" style="top: 0px; height: 10px"></div>
    <div class="decor" style="bottom: 0px; height: 10px"></div>
    <div class="decor" style="bottom: -10px; height: 5px"></div>
    <Container
      style="transform: skewY(11deg); padding-top: 200px; padding-bottom: 200px"
    >
      <div class="col5">
        <div style="display: inline-block">
          <Typography variant="h2" mode="light">Contact Us</Typography>
          <div class="borderBottomRed"></div>
        </div>
        <Typography variant="p" mode="light">
          Jl. Kemenangan No. 33 Medan 20222 Telp. 061-80016938 Fax. 061-80016889
          Email. sinergiindoprima@yahoo.com Web. www.sinergiindoprima.com
        </Typography>
      </div>
      <div class="col5">
        <div style="display: inline-block">
          <Typography variant="h2" mode="light">Kantor Cabang</Typography>
          <div class="borderBottomRed"></div>
        </div>
        <Typography variant="p" mode="light">
          JAKARTA Jl. Kemang Utara IX Blok. AA No. 3A Jakarta 12790 Indonesia
        </Typography>

        <Typography variant="p" mode="light">
          BANDA ACEH Jl. Teuku Nyak Arief No. 24 A Lam Gugop, Kota Banda Aceh
        </Typography>

        <Typography variant="p" mode="light">
          PEKANBARU - RIAU Jl. Arifin Ahmad No. 9 (Gd. Nusantara Lt.3) Pekanbaru
          - Riau
        </Typography>

        <Typography variant="p" mode="light">
          KODYA SIBOLGA Jl. Jend. Sudirman AEK Parambunan - Kodya Sibolga
        </Typography>
      </div>
    </Container>
  </div>
</template>

<script setup>
import Container from "./Container.vue";
import Typography from "./Typography.vue";
import Team from "../assets/team.png";
import Building from "../assets/building-artwork.png";
</script>

<style scoped>
.contact-wrapper {
  box-sizing: border-box;
  position: relative;
  background-color: #020b4a;
  background-image: linear-gradient(to right, #020b4a, rgba(90, 0, 130, 1));
  transform: skewY(-11deg);
  color: #ffffff;
}
.decor {
  position: absolute;
  left: 0px;
  width: 100%;
  background-color: rgba(255, 0, 100, 1);
  background-image: linear-gradient(
    to right,
    rgba(255, 0, 100, 1),
    rgba(40, 0, 170, 1)
  );
}
.team {
  transform: skewY(11deg);
  width: 700px;
  height: auto;
  position: absolute;
  z-index: 400;
  top: -200px;
  left: 50%;
  margin-left: -350px;
}

@media only screen and (max-width: 760px) {
  .team {
    width: 250px;
    margin-left: -125px;
    top: 50px;
  }
}
</style>
