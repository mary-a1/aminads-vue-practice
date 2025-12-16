<!-- Main hero section wrapper -------------------->
<template>
  <section class="hero">
    <div class="hero-inner container">
      <p class="tagline">WEB & DIGITAL PRODUCT DESIGN STUDIO</p>

      <h1 class="title">
        Building <br />
        Modern <br />
        <span class="highlight">Digital</span> <br />
        Experiences
      </h1>

      <p class="description">
        We design and build high-quality websites and digital products for
        ambitious brands.
      </p>

      <div class="buttons">
        <button class="primary">Start a Project</button>
        <button class="secondary">View Work</button>
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
   HERO — WOW PASS
   ========================= */

.hero {
  position: relative;
  padding-block: calc(var(--space-xl) * 1.5);
  overflow: hidden;
}

/* Soft glow anchor */
.hero::before {
  content: "";
  position: absolute;
  top: -20%;
  left: 50%;
  transform: translateX(-50%);
  width: 60rem;
  height: 60rem;
  background: radial-gradient(
    circle,
    rgba(124, 58, 237, 0.12),
    transparent 60%
  );
  z-index: 0;
}

.hero-inner {
  position: relative;
  max-width: 46rem;
  z-index: 1;
}

/* Tagline */
.tagline {
  font-size: var(--text-xs);
  letter-spacing: 0.14em;
  font-weight: 600;
  color: var(--color-primary-soft);
  margin-bottom: var(--space-sm);
}

/* Headline */
.title {
  font-size: var(--text-4xl);
  font-weight: 900;
  line-height: 1.02;
  margin: 0;
}

.highlight {
  color: var(--color-primary);
}

/* Supporting copy */
.description {
  margin-top: var(--space-md);
  font-size: var(--text-lg);
  color: var(--color-text-muted);
  max-width: 36rem;
}

/* CTA group */
.buttons {
  margin-top: var(--space-xl);
  display: flex;
  gap: var(--space-md);
  flex-wrap: wrap;
}

/* Primary CTA — dominant */
.primary {
  background: #111;
  color: white;
  padding: 1rem 2rem;
  border-radius: var(--radius-md);
  font-size: var(--text-base);
  font-weight: 600;
  border: none;
}

/* Secondary CTA — quieter */
.secondary {
  background: transparent;
  border: 1px solid var(--color-border);
  padding: 1rem 1.75rem;
  border-radius: var(--radius-md);
  font-size: var(--text-base);
}

/* =========================
   TABLET
   ========================= */
@media (min-width: 48rem) {
  .hero-inner {
    max-width: 54rem;
  }

  .title {
    font-size: 4.5rem;
  }

  .buttons {
    gap: var(--space-lg);
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 75rem) {
  .hero {
    padding-block: calc(var(--space-xl) * 2);
  }

  .hero-inner {
    text-align: center;
    margin-inline: auto;
  }

  .description {
    margin-inline: auto;
  }

  .buttons {
    justify-content: center;
  }
}

</style>
