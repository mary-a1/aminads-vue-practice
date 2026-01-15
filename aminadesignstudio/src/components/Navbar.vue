<!-- The navigation bar wrapper. ---------------------------->
<template>
  <nav class="navbar">
    <!-- Use the global container for consistent padding + max-width -->
    <div class="navbar-inner container">
      <!-- Brand logo -->
      <div class="brand">
        <img src="/src/assets/images/logo.png" alt="Amina Design Co." class="logo" />
        <div class="brand-text">
          <span class="brand-name">Amina Design Studio Co.</span>
          <span class="badge">Independent studio</span>
        </div>
      </div>
      <button class="menu-toggle" @click="menuOpen = true" aria-label="Open menu">☰</button>

      <button class="cta desktop-only" href="#contact">Book intro call</button>
    </div>
  </nav>

  <!-- MOBILE MENU OVERLAY -->
  <transition name="menu">
    <div
      v-if="menuOpen"
      class="mobile-menu-backdrop"
      @click.self="closeMenu"
    >
      <aside class="mobile-menu">
        <div class="menu-header">
          <div class="brand">
            <img src="/src/assets/images/logo.png" class="logo" />
            <span class="brand-name">Amina Design Co.</span>
          </div>

          <button class="close" @click="closeMenu">✕</button>
        </div>

        <nav class="menu-links">
          <a href="#projects" @click="closeMenu">Portfolio</a>
          <a href="#services" @click="closeMenu">Services</a>
          <a href="#about" @click="closeMenu">The Studio</a>
          <a href="#contact" @click="closeMenu">Contact</a>
        </nav>

        <div class="menu-actions">
          <button class="primary" href="#contact">Start a project</button>
          <button class="secondary" href="#contact">Book intro call</button>
        </div>
      </aside>
    </div>
  </transition>

</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "Navbar",
  data() {
    return {
      menuOpen: false,
    };
  },
  methods: {
    toggleMenu() {
      this.menuOpen = !this.menuOpen;
    },
    closeMenu() {
      this.menuOpen = false;
    },
  },
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* ======================
   NAVBAR (Mobile-first)
====================== */

.navbar {
  position: sticky;
  top: 0;
  z-index: 40;

  /* Floating glass effect */
  background: linear-gradient(
    180deg,
    rgba(12, 17, 32, 0.6),
    rgba(12, 17, 32, 0.25)
  );
  backdrop-filter: blur(14px);
  border-bottom: 1px solid rgba(255, 255, 255, 0.04);
}

.navbar-inner {
  display: flex;
  align-items: center;
  justify-content: space-between;

  padding: 0.75rem 1rem;
  background: transparent;
}

/* ======================
   BRAND
====================== */

.brand {
  display: flex;
  align-items: center;
  gap: 0.75rem;
  min-width: 0;
}

.logo {
  height: 2.2rem;
  flex-shrink: 0;
}

.brand-name {
  font-weight: 700;
  font-size: 0.95rem;
  white-space: nowrap;
  color: #e5e7eb;
  margin-right: 0.25rem; /* subtle breathing room */
}

.badge {
  display: none; /* hidden by default (mobile-first) */
  align-items: center;
  gap: 0.35rem;

  padding: 0.35rem 0.65rem;
  border-radius: 999px;

  font-size: 0.75rem;
  font-weight: 500;
  letter-spacing: 0.02em;

  color: rgba(226, 232, 240, 0.75);
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.08);
}

.badge::before {
  content: "•";
  color: #38bdf8;
  font-size: 1rem;
  line-height: 0;
}


/* ======================
   ACTIONS (Mobile default)
====================== */

/* Mobile: hamburger visible */
.menu-toggle {
  display: inline-flex;
  background: none;
  border: none;
  font-size: 1.6rem;
  color: #e5e7eb;
}

/* Mobile: CTA hidden */
.cta {
  display: none;
}

/* ======================
   MOBILE MENU
====================== */

.mobile-menu-backdrop {
  position: fixed;
  inset: 0;
  z-index: 50;
  background: rgba(5, 8, 20, 0.6);
  backdrop-filter: blur(6px);
  display: flex;
  justify-content: flex-end;
}

.mobile-menu {
  width: min(88%, 360px);
  height: 100%;
  background: linear-gradient(160deg, #0f172a, #111827);
  padding: 1.25rem;

  display: flex;
  flex-direction: column;
  gap: 1.5rem;

  box-shadow: -20px 0 60px rgba(0, 0, 0, 0.5);
}

/* Header */
.menu-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.close {
  background: none;
  border: none;
  font-size: 1.4rem;
  color: #e5e7eb;
}

/* Links */
.menu-links {
  display: flex;
  flex-direction: column;
  gap: 1rem;
}

.menu-links a {
  font-size: 1.1rem;
  font-weight: 600;
  color: #e5e7eb;
  text-decoration: none;
}

/* Actions */
.menu-actions {
  margin-top: auto;
  display: grid;
  gap: 0.75rem;
}

.menu-actions .primary {
  padding: 0.85rem;
  border-radius: 14px;
  border: none;
  font-weight: 700;
  background: linear-gradient(135deg, #a855f7, #38bdf8);
  color: #0f172a;
}

.menu-actions .secondary {
  padding: 0.85rem;
  border-radius: 14px;
  border: 1px solid rgba(255, 255, 255, 0.18);
  background: rgba(255, 255, 255, 0.04);
  color: #e5e7eb;
}

/* ======================
   ANIMATION
====================== */

.menu-enter-active,
.menu-leave-active {
  transition: opacity 0.25s ease;
}
.menu-enter-from,
.menu-leave-to {
  opacity: 0;
}

/* ======================
   DESKTOP OVERRIDE
====================== */

@media (min-width: 768px) {
  /* Desktop: show CTA */
  .cta {
    display: inline-flex;
    align-items: center;
    gap: 0.35rem;

    border: none;
    border-radius: 14px;
    padding: 0.75rem 1.2rem;
    font-weight: 700;

    background: linear-gradient(135deg, #a855f7, #38bdf8);
    color: #0f172a;
    box-shadow: 0 12px 24px rgba(56, 189, 248, 0.35);
  }

  /* Desktop: hide hamburger */
  .menu-toggle {
    display: none;
  }

  .logo {
    height: 3rem;
  }

  .navbar-inner {
    padding: 0.9rem 1.15rem;
  }
  .badge {
    display: inline-flex;
  }
}

@media (min-width: 1200px) {
  .logo {
    height: 3.5rem;
  }
}

</style>
