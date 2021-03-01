<template>
  <div class="card-surah">
    <b-card class="card-surah">
      <b-card-title
        >{{ surah.nama }} <strong>({{ surah.asma }})</strong></b-card-title
      >
      <b-card-sub-title class="mb-2">{{ surah.type }}</b-card-sub-title>
      <b-card-text>
        {{ surah.nama }} <strong>({{ surah.asma }})</strong>, memiliki arti
        {{ surah.arti }} dan <strong>{{ surah.ayat }} ayat</strong>
      </b-card-text>

      <router-link class="btn btn-lg btn-success" :to="'/Surah/'+surah.nomor"> Mulai Baca </router-link>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "CardSurah",
  props: ["surah"],
};
</script>

<style>
</style>