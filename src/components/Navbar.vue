<template>
  <div class="container">
    <b-navbar toggleable="lg">
      <b-navbar-brand href="/"><b> Home </b></b-navbar-brand>

      <b-navbar-toggle target="nav-collapse"></b-navbar-toggle>

      <b-collapse id="nav-collapse" is-nav>
        <b-navbar-nav>
          <b-nav-item href="/Al-Quran">Al-Quran</b-nav-item>
          <b-nav-item href="#" disabled>Kisah Nabi</b-nav-item>
        </b-navbar-nav>
      </b-collapse>
    </b-navbar>
  </div>
</template>

<script>
export default {
  name: "Navbar",
};
</script>

<style>
</style>