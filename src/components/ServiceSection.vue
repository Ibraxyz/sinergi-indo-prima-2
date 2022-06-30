<template>
  <div style="box-sizing: border-box; padding-top: 0px">
    <div style="text-align: center">
      <Typography variant="h2" mode="dark" sx="color:#01579B">Our Services</Typography>
    </div>
    <div class="borderBottomRed"></div>

    <div class="service-section">
      <div
        class="section-individual"
        style="
          background-color: rgba(227, 242, 253, 0.3);
          position: relative;
          overflow: hidden;
        "
      >
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
          <div class="col5" style="position: relative">
            <Typography variant="h3" mode="dark" sx="color:#01579B"
              >Customer Service</Typography
            >
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B;font-weight:100"
              >Pelajari lebih lanjut</Typography
            >
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

            <!-- triangle image -->
            <TriangleCornerImage :img="Cs" />
          </div>
        </Container>
      </div>

      <div class="section-individual">
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg vertical 2 -->
            <DecorLineBg to="bottom" width="10px" height="400px" top="-20%" right="30%" />

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
              height="400px"
              bottom="-25%"
              right="-30%"
            />
            <!-- triangle image -->
            <TriangleCornerImage :img="Pp" triangleColor="#fafafa" />
          </div>
          <div class="col5">
            <Typography variant="h3" mode="dark" sx="color:#01579B"
              >Pelatihan Pendidikan</Typography
            >
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B"
              >Pelajari lebih lanjut</Typography
            >
          </div>
        </Container>
      </div>

      <div
        class="section-individual"
        style="
          background-color: rgba(227, 242, 253, 0.3);
          position: relative;
          overflow: hidden;
        "
      >
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
          <div class="col5" style="position: relative">
            <Typography variant="h3" mode="dark" sx="color:#01579B">Satpam</Typography>
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B;font-weight:100"
              >Pelajari lebih lanjut</Typography
            >
          </div>
          <div class="col5" style="position: relative">
            <!-- image describing feature on the side -->

            <!-- container -->

            <!-- line decor bg horizontal satpam-->
            <DecorLineBg to="right" top="50%" left="-30%" height="10px" width="100%" />

            <!-- line decor bg vertical satpam -->
            <DecorLineBg to="bottom" width="10px" height="400px" top="50%" right="130%" />

            <!-- triangle image -->
            <TriangleCornerImage :img="Satpam" />
          </div>
        </Container>
      </div>

      <div class="section-individual">
        <Container noPadding>
          <div class="col5" style="position: relative">
            <!-- line decor bg vertical 2 -->
            <DecorLineBg to="bottom" width="10px" height="400px" top="-20%" right="30%" />

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
              height="400px"
              bottom="-25%"
              right="-30%"
            />
            <!-- triangle image -->
            <TriangleCornerImage :img="CleaningService" triangleColor="#fafafa" />
          </div>
          <div class="col5">
            <Typography variant="h3" mode="dark" sx="color:#01579B"
              >Cleaning Service</Typography
            >
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B"
              >Pelajari lebih lanjut</Typography
            >
          </div>
        </Container>
      </div>

      <div
        class="section-individual"
        style="
          background-color: rgba(227, 242, 253, 0.3);
          position: relative;
          overflow: hidden;
        "
      >
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
            <DecorLineBg to="right" top="150%" left="59.8%" width="100%" height="10px" />
            <!-- line decor bg vertical bottom 3 -->
            <DecorLineBg
              to="bottom"
              width="10px"
              height="400px"
              bottom="-248%"
              right="38.2%"
            />
            <Typography variant="h3" mode="dark" sx="color:#01579B"
              >Karyawan Perkantoran</Typography
            >
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B"
              >Pelajari lebih lanjut</Typography
            >
          </div>
          <div class="col5">
            <!-- triangle image -->
            <TriangleCornerImage :img="KaryawanPerkantoran" />
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
            <TriangleCornerImage :img="Sales" triangleColor="#fafafa" />
          </div>
          <div class="col5">
            <Typography variant="h3" mode="dark" sx="color:#01579B"
              >Sales Promotion dan Office Support</Typography
            >
            <Typography variant="p" mode="dark">
              Perusahaan penyedia jasa prima, handal, baik dan profesional serta memiliki
              standard nasional dan terpercaya.
            </Typography>
            <Typography variant="span" mode="dark" sx="color:#01579B"
              >Pelajari lebih lanjut</Typography
            >
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
import TriangleCornerImage from "./TriangleCornerImage.vue";
import DecorLineBg from "./DecorLineBg.vue";
import Satpam from "../assets/gambar1.png";
import CleaningService from "../assets/cleaningservice.png";
import Cs from "../assets/cs.png";
import KaryawanPerkantoran from "../assets/karyawan-perkantoran.png";
import Sales from "../assets/sales.png";
import Pp from "../assets/pp3.png";
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
