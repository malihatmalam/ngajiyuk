<template>
  <div class="quran">
    <Navbar />
    <div class="container">
      <QuranHeader />
      <div class="row mt-4">
        <div class="col">
          <h2><Strong> Surah </Strong></h2>
        </div>
      </div>
      <div class="row mb-3">
        <div class="col-md-4 mt-4" v-for="surah in surahs" :key="surah.nomor">
          <CardSurah :surah="surah"/>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
import Navbar from "@/components/Navbar.vue";
import QuranHeader from "@/components/QuranHeader.vue";
import CardSurah from "@/components/CardSurah.vue";
import axios from "axios";

export default {
  name: "Quran",
  components: {
    Navbar,
    QuranHeader,
    CardSurah,
  },
  data() {
    return {
      surahs: [],
    };
  },
  methods: {
    setSurahs(data) {
      this.surahs = data;
    },
  },
  mounted() {
    axios
      .get("https://api.npoint.io/99c279bb173a6e28359c/data")
      .then((response) =>
        this.setSurahs(response.data)
      )
      .catch((error) =>
        // handle error
        console.log("Gagal : ",error)
      )
  },
};
</script>

<style>
</style>