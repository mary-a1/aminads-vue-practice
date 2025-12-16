<!-- Wrapper for the whole section -->
<!-- Wrapper for the whole section -->
<template>
  <section class="section">
    <!-- Inner wrapper helps us center content on desktop -->
    <div class="section-inner">

      <!-- Section title -->
      <h2 class="section-title">✨ Featured Projects</h2>

      <!-- Project list wrapper -->
      <div class="projects">
        <ProjectCard
          title="Amal Transfers"
          subtitle="Full-stack money transfer platform (FinTech)"
          description="UX/UI, product design, and full web implementation."
          url="https://amaltransfers.ca"
          logo="/src/assets/images/amal-logo.png"
        />

        <ProjectCard
          title="Maalin Active"
          subtitle="E-commerce brand & product experience"
          description="Shopify storefront, product experience, and brand system."
          url="https://maalinactive.com"
          logo="/src/assets/images/maalin-logo.png"
        />

        <ProjectCard
          title="Nasriina Studio"
          subtitle="Creative portfolio & digital operations"
          description="Website, LinkedIn, pricing system, and digital portfolio."
          url="#"
          logo="/src/assets/images/nasriina-logo.png"
        />
      </div>

    </div>
  </section>
</template>



<!-- Options API format ----------------------------------->
<script>
  // You manually import components in pure Vue
  import ProjectCard from "./ProjectCard.vue"

  export default {
    name: "FeaturedProjects",
    // Register imported components so Vue can use them
    components: {
      ProjectCard
    }
}
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* =========================
   MOBILE (default)
   ========================= */

.section {
  padding: 24px;
}

.section-title {
  font-size: clamp(1.25rem, 3vw, 2rem);
  font-weight: 800;
  letter-spacing: -0.02em;
  margin-bottom: var(--space-xl);
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
}
.section-title::after {
  content: "";
  display: block;
  height: 3px;
  width: 48px;
  margin-top: 8px;
  border-radius: 999px;
  background: linear-gradient(
    90deg,
    var(--color-accent),
    transparent
  );
}
/* Stack cards vertically */
.projects {
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.project-logo {
  width: 7rem;
  height: 7rem;
  border-radius: 999px;
  display: flex;
  align-items: center;
  justify-content: center;
  background: radial-gradient(
    circle at top,
    rgba(255, 215, 0, 0.18),
    rgba(255, 215, 0, 0.05),
    transparent 70%
  );
  position: relative;
}
.project-logo::after {
  content: "";
  position: absolute;
  inset: 0;
  border-radius: inherit;
  box-shadow:
    0 0 0 1px rgba(255, 215, 0, 0.25),
    0 12px 30px rgba(255, 215, 0, 0.25);
  opacity: 0.35;
  pointer-events: none;
}

.project-logo img {
  max-width: 70%;
  max-height: 70%;
  object-fit: contain;
  z-index: 1;
}

/* =========================
   TABLET (iPad)
   ========================= */
@media (min-width: 768px) {
  .section {
    padding: 48px 40px;
  }

  .section-title {
    font-size: 24px;
    margin-bottom: 24px;
  }

  .projects {
    gap: 24px;
  }
}

@media (max-width: 48rem) {
  .project-logo {
    width: 5.5rem;
    height: 5.5rem;
    margin-bottom: var(--space-md);
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 1200px) {
  .section {
    padding: 80px 0;
  }

  .section-inner {
    max-width: 900px;
    margin: 0 auto;
  }

  .section-title {
    font-size: 28px;
  }

  .projects {
    gap: 32px;
  }
}
</style>

