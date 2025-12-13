<!-- Wrapper for the entire studio/about section ------>
<template>
  <section class="studio">

    <!-- Section heading -->
    <h2 class="title">The Studio</h2>

    <!--
      Main body text
      Matches your portfolio’s paragraph layout
    -->
    <p class="body">
      Amina Design Co. is a Toronto-based web and digital product design studio
      specializing in crafting exceptional digital experiences for modern brands.

      <br /><br />

      Our approach combines strategic thinking, beautiful design, and robust
      development to deliver solutions that scale.

      <br /><br />

      Whether you're launching a new platform, refreshing your digital presence,
      or building a product from the ground up, we bring the expertise and
      attention to detail needed to bring your vision to life.
    </p>

  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
  export default {
    name: "StudioSection"
  }
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
  .studio {
    padding: 24px;
  }

  .title {
    font-size: 22px;
    font-weight: 700;
    margin-bottom: 16px;
  }

  .body {
    color: #666;
    line-height: 1.6;
    font-size: 15px;
  }
</style>
