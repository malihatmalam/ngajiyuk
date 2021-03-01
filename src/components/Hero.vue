<template>
  <div class="hero">
    <!--Dekstop -->
    <div class="d-none d-md-block">
      <div class="row mt-4">
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <strong> Ngaji Yuk, </strong> Karena <br />
                " ilmu adalah kehidupan bagi pikiran "
              </h2>
              <h4>(Abu Bakar)</h4>
              <p class="mt-4">Ayo Mengaji Besama Kami</p>
              <a href="/Al-Quran" class="btn btn-lg btn-standar">
                <b-icon-arrow-right-circle></b-icon-arrow-right-circle> Mulai
                Mengaji
              </a>
            </div>
          </div>
        </div>
        <div class="col-md-6">
          <img src="../assets/images/Hero.png" width="100%" alt="Ngaji Yuk" />
        </div>
      </div>
    </div>

    <!-- Mobile -->
    <div class="d-sm-block d-md-none">
      <div class="row mt-4">
        <div class="col-md-6 mb-1">
          <img src="../assets/images/Hero.png" width="100%" alt="Ngaji Yuk" />
        </div>
        <div class="col-md-6">
          <div class="d-flex h-100">
            <div class="justify-content-center align-self-center">
              <h2>
                <br />
                <strong> Ngaji Yuk, </strong> Karena <br />
                " ilmu adalah kehidupan bagi pikiran "
              </h2>
              <h4>(Abu Bakar)</h4>
              <p class="mt-4">Ayo Mengaji Besama Kami</p>
              <a href="/Al-Quran" class="btn btn-lg btn-standar">
                <b-icon-arrow-right-circle></b-icon-arrow-right-circle> Mulai
                Mengaji
              </a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style>
</style>