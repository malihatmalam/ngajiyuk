<template>
  <div class="hero">
    <!--Dekstop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong> Al-Quran Ku, </strong> <br />
                mari mengaji Al-Quran bersama kami.
              </h2>
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
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong> Al-Quran Ku, </strong> <br />
                mari mengaji Al-Quran bersama kami.
              </h2>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "SurahHeader",
};
</script>

<style>
</style>