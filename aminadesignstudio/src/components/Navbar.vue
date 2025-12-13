<!-- The navigation bar wrapper. ---------------------------->
<template>
  <nav class="navbar">
    <div class="navbar-inner">
      <!-- Brand logo -->
      <img src="/src/assets/images/logo.png" alt="Amina Design Studio" class="logo" />

      <!-- Future nav / CTA goes here -->
      <!-- Keeping structure ready is intentional -->
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
/* =========================
   BASE (Mobile-first)
   ========================= */

.navbar {
  padding: 1rem 1.5rem; /* 16px 24px */
}

.navbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

/* Logo */
.logo {
  height: 2rem; /* 32px */
  display: block;
}

/* =========================
   TABLET
   ========================= */
@media (min-width: 768px) {
  .navbar {
    padding: 1.5rem 2.5rem; /* 24px 40px */
  }

  .logo {
    height: 2.5rem; /* 40px */
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 1200px) {
  .navbar {
    padding: 2rem 0;
  }

  .navbar-inner {
    max-width: 75rem; /* 1200px */
    margin: 0 auto;
  }

  .logo {
    height: 3rem; /* 48px */
  }
}
</style>
