<!-- The navigation bar wrapper. ---------------------------->
<template>
  <nav class="navbar">

    <!-- The logo image -->
    <img
      src="/src/assets/images/logo.png"
      alt="Logo"
      class="logo"
    />
  </nav>
</template>

<!-- Options API format ----------------------------------->
<script>
  export default {
    // Component name (optional but good practice)
    name: "Navbar"
  }
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>

  .navbar {
    padding: 16px;
  }

  .logo {
    width: 32px; /* controls the size of the logo */
  }
</style>
