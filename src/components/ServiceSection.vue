<template>
  <div style="box-sizing: border-box; padding-top: 0px">
    <div style="text-align: center">
      <Typography variant="h2" mode="light">Our Services</Typography>
    </div>
    <div class="borderBottomRed"></div>

    <div class="service-section">
      <div class="section-individual" style="position: relative; overflow: hidden">
        <!-- decorative bg -->
        <img
          src="../assets/g-decor.png"
          alt=""
          style="
            position: absolute;
            top: 100px;
            left: 20%;
            width: 100%;
            height: auto;
            z-index: -1;
            opacity: 0.1;
          "
        />

        <Container noPadding>
          <div class="col5" style="position: relative">
            <Typography variant="h3" mode="light">Customer Service</Typography>
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
          <div class="col5" style="position: relative">
            <!-- image describing feature on the side -->

            <!-- container -->

            <!-- line decor bg vertical satpam-->
            <DecorLineBg
              to="bottom"
              top="-100px"
              left="50%"
              right="50%"
              height="50%"
              width="10px"
            />
            <!-- end of line decor bg vertical -->

            <!-- line decor bg horizontal satpam-->
            <DecorLineBg to="right" top="50%" left="-30%" height="10px" width="100%" />

            <!-- line decor bg vertical satpam -->
            <DecorLineBg to="bottom" width="10px" height="400px" top="50%" right="130%" />

            <!-- image -->
            <DecoratedImg :img="Cs" />
          </div>
        </Container>
      </div>

      <div class="section-individual">
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg vertical 2 -->
            <DecorLineBg to="bottom" width="10px" height="200px" top="-20%" right="30%" />

            <!-- line decor bg horizontal 2-->
            <DecorLineBg
              :reverse="true"
              to="left"
              width="100%"
              height="10px"
              top="50%"
              left="30%"
            />

            <!-- line decor bg vertical bottom 2 -->
            <DecorLineBg
              to="bottom"
              width="10px"
              height="280px"
              bottom="-45%"
              right="-30%"
            />
            <!-- triangle image -->
            <DecoratedImg :img="Pp" triangleColor="#fafafa" />
          </div>
          <div class="col5">
            <Typography variant="h3" mode="light">Pelatihan Pendidikan</Typography>
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
        </Container>
      </div>

      <div class="section-individual" style="position: relative; overflow: hidden">
        <!-- decorative bg -->
        <img
          src="../assets/g-decor.png"
          alt=""
          style="
            position: absolute;
            top: 100px;
            left: 20%;
            width: 100%;
            height: auto;
            z-index: -1;
            opacity: 0.15;
          "
        />

        <Container noPadding>
          <div class="col5" style="position: relative; z-index: 200">
            <Typography variant="h3" mode="light">Satpam</Typography>
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
          <div class="col5" style="position: relative">
            <!-- image describing feature on the side -->

            <!-- container -->

            <!-- line decor bg horizontal satpam-->
            <DecorLineBg to="right" top="70%" left="-30%" height="10px" width="100%" />

            <!-- line decor bg vertical satpam -->
            <DecorLineBg to="bottom" width="10px" height="400px" top="70%" right="130%" />

            <!-- triangle image -->
            <DecoratedImg :img="Satpam" />
          </div>
        </Container>
      </div>

      <div class="section-individual">
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg vertical 2 -->
            <DecorLineBg to="bottom" width="10px" height="300px" top="-20%" right="30%" />

            <!-- line decor bg horizontal 2-->
            <DecorLineBg
              :reverse="true"
              to="left"
              width="100%"
              height="10px"
              top="60%"
              left="30%"
            />

            <!-- line decor bg vertical bottom 2 -->
            <DecorLineBg
              to="bottom"
              width="10px"
              height="300px"
              bottom="-72%"
              right="-30%"
            />
            <!-- triangle image -->
            <DecoratedImg :img="CleaningService" triangleColor="#fafafa" />
          </div>
          <div class="col5" style="position: relative; z-index: 200">
            <Typography variant="h3" mode="light">Cleaning Service</Typography>
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
        </Container>
      </div>

      <div class="section-individual" style="position: relative; overflow: hidden">
        <!-- decorative bg -->
        <img
          src="../assets/g-decor.png"
          alt=""
          style="
            position: absolute;
            top: 100px;
            left: 20%;
            width: 100%;
            max-width: 100%;
            height: auto;
            z-index: -1;
            opacity: 0.15;
          "
        />
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg horizontal bottom 3-->
            <DecorLineBg to="right" top="128%" left="59.8%" width="100%" height="10px" />
            <!-- line decor bg vertical bottom 3 -->
            <DecorLineBg
              to="bottom"
              width="10px"
              height="400px"
              bottom="-248%"
              right="38.2%"
            />
            <Typography variant="h3" mode="light">Karyawan Perkantoran</Typography>
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
          <div class="col5">
            <!-- triangle image -->
            <DecoratedImg :img="KaryawanPerkantoran" />
          </div>
        </Container>
      </div>

      <div class="section-individual">
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg vertical bottom 4 -->
            <DecorLineBg
              to="bottom"
              width="10px"
              height="400px"
              top="-20%"
              right="38.2%"
            />
            <!-- triangle image -->
            <DecoratedImg :img="Sales" triangleColor="#fafafa" />
          </div>
          <div class="col5" style="position: relative; z-index: 200">
            <Typography variant="h3" mode="light"
              >Sales Promotion dan Office Support</Typography
            >
            <Typography variant="p" mode="light">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
          </div>
        </Container>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Container from "./Container.vue";
import Typography from "./Typography.vue";
import DecorLineBg from "./DecorLineBg.vue";
import Satpam from "../assets/gambar1.png";
import CleaningService from "../assets/cleaningservice.png";
import Cs from "../assets/cs.png";
import KaryawanPerkantoran from "../assets/karyawan-perkantoran.png";
import Sales from "../assets/sales.png";
import Pp from "../assets/pp3.png";
import DecoratedImg from "./DecoratedImg.vue";
</script>

<style scoped>
.borderBottomRed {
  width: 50px;
  border-bottom: 3px solid red;
  margin-top: 3px;
  margin-right: auto;
  margin-left: auto;
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

.service-section {
  /** background-color: #e3f2fd; **/
  box-sizing: border-box;
  padding: 40px 0px 40px 0px;
}

.section-individual {
  box-sizing: border-box;
  padding: 40px 15px 40px 15px;
}
</style>
