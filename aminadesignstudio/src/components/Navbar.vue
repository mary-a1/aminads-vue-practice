<!-- The navigation bar wrapper. ---------------------------->
<template>
  <nav class="navbar">
    <!-- Use the global container for consistent padding + max-width -->
    <div class="navbar-inner container">
      <!-- Brand logo -->
      <img src="/src/assets/images/logo.png" alt="Amina Design Studio" class="logo" />

      <!-- Future nav / CTA goes here -->
    </div>
  </nav>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  // Component name (optional but good practice)
  name: "Navbar",
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* Full-width nav wrapper */
.navbar {
  padding-block: var(--space-md);
}

/* Inner layout: keeps logo aligned + allows future nav/CTA */
.navbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* Logo sizing (scales by breakpoint) */
.logo {
  height: 2.5rem; /* ~40px */
  display: block;
}

@media (min-width: 768px) {
  .logo {
    height: 3rem; /* ~48px */
  }
}

@media (min-width: 1200px) {
  .logo {
    height: 3.5rem; /* ~56px */
  }
}
</style>
