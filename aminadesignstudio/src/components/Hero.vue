<!-- Main hero section wrapper -------------------->
<template>
  <section class="hero">
    <div class="hero-inner">
      <p class="tagline">WEB & DIGITAL PRODUCT DESIGN STUDIO</p>

      <h1 class="title">
        Building <br />
        Modern <br />
        <span class="highlight">Digital</span> <br />
        Experiences
      </h1>

      <p class="description">
        From fintech platforms to e-commerce brands — we design and build exceptional websites and
        digital products.
      </p>

      <div class="buttons">
        <button class="primary">Start a Project</button>
        <button class="secondary">View Our Work</button>
      </div>

      <LocationTag />
    </div>
  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
import LocationTag from "./LocationTag.vue";

export default {
  name: "Hero",
  components: {
    LocationTag,
  },
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* =========================
   BASE (Mobile-first)
   ========================= */

.hero {
  padding: 1.5rem; /* 24px */
}

.hero-inner {
  max-width: 100%;
}

/* Tagline */
.tagline {
  color: #6b46ff;
  font-size: 0.75rem; /* 12px */
  letter-spacing: 0.08em;
  font-weight: 600;
}

/* Main headline */
.title {
  margin-top: 0.75rem;
  font-size: 2.75rem; /* ~44px */
  font-weight: 800;
  line-height: 1.05;
}

/* Accent word */
.highlight {
  color: #7c3aed;
}

/* Supporting copy */
.description {
  margin-top: 1rem;
  font-size: 1rem;
  color: #666;
  line-height: 1.6;
}

/* Buttons */
.buttons {
  margin-top: 1.5rem;
  display: flex;
  flex-direction: column;
  gap: 0.75rem;
}

.primary,
.secondary {
  padding: 0.875rem 1rem;
  border-radius: 0.5rem;
  font-size: 0.95rem;
  font-weight: 600;
}

/* Primary CTA */
.primary {
  background: #111;
  color: #fff;
  border: none;
}

/* Secondary CTA */
.secondary {
  background: #fff;
  border: 1px solid #ddd;
}

/* =========================
   TABLET (iPad)
   ========================= */
@media (min-width: 768px) {
  .hero {
    padding: 4rem 2.5rem;
  }

  .title {
    font-size: 3.5rem; /* ~56px */
  }

  .description {
    font-size: 1.0625rem;
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 1200px) {
  .hero {
    padding: 5rem 0;
    position: relative;
  }

  .hero-inner {
    max-width: 56rem; /* ~896px */
    margin: 0 auto;
    text-align: center;
  }

  .title {
    font-size: 4.5rem; /* 72px */
    max-width: 56rem;
    margin: 0 auto;
  }

  .description {
    font-size: 1.25rem;
    max-width: 40rem;
    margin: 1.5rem auto 0;
  }

  .buttons {
    flex-direction: row;
    justify-content: center;
  }
}
</style>
