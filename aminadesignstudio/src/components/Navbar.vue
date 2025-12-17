<!-- The navigation bar wrapper. ---------------------------->
<template>
  <nav class="navbar">
    <!-- Use the global container for consistent padding + max-width -->
    <div class="navbar-inner container">
      <!-- Brand logo -->
      <div class="brand">
        <img src="/src/assets/images/logo.png" alt="Amina Design Studio" class="logo" />
        <span class="badge">Independent studio</span>
      </div>

      <button class="cta">Book intro call</button>
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
  padding-block: 1rem;
  position: sticky;
  top: 0;
  z-index: 10;
  backdrop-filter: blur(16px);
  background: linear-gradient(180deg, rgba(12, 17, 32, 0.85), rgba(12, 17, 32, 0.6));
}

/* Inner layout: keeps logo aligned + allows future nav/CTA */
.navbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0.75rem 0.85rem;
  border: 1px solid rgba(255, 255, 255, 0.08);
  background: rgba(255, 255, 255, 0.03);
  border-radius: 16px;
  box-shadow: 0 10px 35px rgba(0, 0, 0, 0.25);
}

/* Logo sizing (scales by breakpoint) */
.logo {
  height: 2.5rem; /* ~40px */
  display: block;
}

.brand {
  display: flex;
  align-items: center;
  gap: 0.65rem;
}

.badge {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.4rem 0.65rem;
  border-radius: 999px;
  border: 1px solid rgba(255, 255, 255, 0.1);
  color: rgba(226, 232, 240, 0.85);
  background: rgba(255, 255, 255, 0.04);
  font-size: 0.85rem;
}

.badge::before {
  content: "•";
  color: var(--color-secondary);
  font-size: 1rem;
}

.cta {
  border: none;
  background: linear-gradient(135deg, #a855f7, #38bdf8);
  color: #0f172a;
  font-weight: 700;
  padding: 0.75rem 1.05rem;
  border-radius: 14px;
  box-shadow: 0 12px 24px rgba(56, 189, 248, 0.3);
  cursor: pointer;
}

@media (min-width: 768px) {
  .logo {
    height: 3rem; /* ~48px */
  }

  .navbar-inner {
    padding: 0.9rem 1.15rem;
  }

  .badge {
    font-size: 0.95rem;
  }

  .cta {
    padding: 0.85rem 1.25rem;
  }
}

@media (min-width: 1200px) {
  .logo {
    height: 3.5rem; /* ~56px */
  }
}
</style>
