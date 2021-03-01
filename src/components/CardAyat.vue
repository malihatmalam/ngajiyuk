<template>
  <div class="card-ayat">
    <b-card class="card-ayat ali">
      <b-card-title>
        <strong> {{ ayat.nomor }} </strong>
      </b-card-title>
      <b-card-title class="text-right">
        <strong> {{ ayat.ar }} </strong>
      </b-card-title>
      <!-- <b-card-sub-title class="mb-2 text-right">
        {{ ayat.tr }}
      </b-card-sub-title> -->
      <br />
      <b-card-text>
        <strong> Artinya : </strong> <br>
        {{ ayat.id }}
      </b-card-text>
    </b-card>
  </div>
</template>

<script>
export default {
  name: "CardAyat",
  props: ["ayat"],
};
</script>

<style>
</style>