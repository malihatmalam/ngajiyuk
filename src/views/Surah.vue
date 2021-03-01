<template>
  <div class="surah">
    <Navbar />
    <div class="container">
      <div class="row mt-5">
        <div class="col">
          <!-- Breadcrumb -->
          <b-breadcrumb>
            <b-breadcrumb-item href="/">
              <b-icon
                icon="house-fill"
                scale="1.25"
                shift-v="1.25"
                aria-hidden="true"
              ></b-icon>
              Home
            </b-breadcrumb-item>
            <b-breadcrumb-item href="/Al-Quran">Al-Quran</b-breadcrumb-item>
            <b-breadcrumb-item active>Surah</b-breadcrumb-item>
          </b-breadcrumb>
          <!-- End Breadcrumb -->
        </div>
      </div>
      <div class="row mt-5">
        <!--Dekstop -->
        <div class="d-none d-md-block">
          <div class="row mt-4">
            <div class="col-md-6">
              <div class="d-flex h-100">
                <div class="justify-content-center align-self-center">
                  <h1>
                    <strong> Surah {{ surah.nama }} </strong> (
                    {{ surah.asma }} )
                  </h1>
                  <h2>
                    Artinya = <strong> " {{ surah.arti }} " </strong>
                  </h2>
                  <br />
                  <h4 class="mt-2">
                    Diturunkan di <strong> {{ surah.type }} </strong>, Memiliki
                    <strong> {{ surah.ayat }} ayat </strong>
                  </h4>
                  <p>
                    <strong> Keterangan : </strong>
                    {{ surah.keterangan }}
                  </p>
                </div>
              </div>
            </div>
            <div class="col-md-6">
              <img src="../assets/images/Surah.png" alt="" width="80%" />
            </div>
          </div>
        </div>

        <!-- Mobile -->
        <div class="d-sm-block d-md-none">
          <div class="row mt-4">
            <div class="col-md-6 mb-1">
              <img src="../assets/images/Surah.png" alt="" width="80%" />
            </div>
            <div class="col-md-6 mt-4">
              <div class="d-flex h-100">
                <div class="justify-content-center align-self-center">
                  <h1>
                    <strong> Surah {{ surah.nama }} </strong> (
                    {{ surah.asma }} )
                  </h1>
                  <h2>
                    Artinya = <strong> " {{ surah.arti }} " </strong>
                  </h2>
                  <br />
                  <h4 class="mt-2">
                    Diturunkan di <strong> {{ surah.type }} </strong>, Memiliki
                    <strong> {{ surah.ayat }} ayat </strong>
                  </h4>
                  <p>
                    <strong> Keterangan : </strong>
                    {{ surah.keterangan }}
                  </p>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
      <div class="row mt-4">
        <div class="col">
          <h2><Strong> Ayat - Ayat Surah {{ surah.nama }} ({{ surah.asma }}) </Strong></h2>
        </div>
      </div>
      <div class="row mb-3">
        <div class="col-md-12 mt-4" v-for="ayat in ayats" :key="ayat.nomor">
          <CardAyat :ayat="ayat" />
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import Navbar from "@/components/Navbar.vue";
import CardAyat from "@/components/CardAyat.vue";
import axios from "axios";

export default {
  name: "Surah",
  components: {
    Navbar,
    CardAyat,
  },
  //   dataSurah() {
  //     return {
  //       surah: [],
  //     };
  //   },
  data() {
    return {
      surah: [],
      ayats: [],
    };
  },
  methods: {
    setAyats(data) {
      this.ayats = data;
    },
    setSurah(data) {
      this.surah = data;
    },
  },
  mounted() {
    axios
      .get(
        "https://api.npoint.io/99c279bb173a6e28359c/surat/" +
          this.$route.params.id
      )
      .then((response) => this.setAyats(response.data))
      .catch((error) =>
        // handle error
        console.log("Gagal : ", error)
      );

    axios
      .get(
        "https://api.npoint.io/99c279bb173a6e28359c/data/" +
          (this.$route.params.id - 1)
      )
      .then((response) => this.setSurah(response.data))
      .catch((error) =>
        // handle error
        console.log("Gagal : ", error)
      );
  },
};
</script>

<style>
</style>