<!-- Wrapper for the whole section -->
<!-- Wrapper for the whole section -->
<template>
  <section id="projects" class="section">
    <!-- Inner wrapper helps us center content on desktop -->
    <div class="container">
      <div class="section-inner">
        <!-- Section title -->
        <div class="section-headline">
          <p class="eyebrow">Selected launches</p>
          <h2 class="section-title">Featured Projects</h2>
          <p class="section-subtitle">
            Case studies focused on launch-ready SaaS, fintech, and commerce platforms.
          </p>
        </div>

        <!-- Project list wrapper -->
        <div class="projects">
          <ProjectCard
            title="Amal Transfers"
            primaryTag="Fintech Platform"
            secondaryTag="Shipped Product"
            subtitle="End-to-end fintech platform"
            description="Design and build of a live money transfer platform, covering product strategy, UX, and full web implementation."
            url="https://amaltransfers.ca"
            logo="/src/assets/images/amal-logo.png"
          />

          <ProjectCard
            title="Maalin Active"
            primaryTag="E-commerce Platform"
            secondaryTag="Shipped Experience"
            subtitle="E-commerce brand and product experience"
            description="A conversion-focused Shopify experience spanning brand, storefront design, and product flows."
            url="https://maalinactive.com"
            logo="/src/assets/images/maalin-logo.png"
          />

          <ProjectCard
            title="Nasriina Studio"
            primaryTag="Digital Platform"
            secondaryTag="Shipped Experience"
            subtitle="Digital platform and operational systems"
            description="A complete digital presence including website, pricing structure, and client-facing workflows."
            url="https://nasrinastudio.com/"
            logo="/src/assets/images/nasriina-logo.png"
          />
        </div>
      </div>
    </div>
  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
import ProjectCard from "./ProjectCard.vue";

export default {
  name: "FeaturedProjects",
  components: {
    ProjectCard,
  },
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>

/* =========================
   MOBILE (default)
   ========================= */

.section {
  padding: clamp(1.5rem, 5vw, 3rem) 0;
  padding-block: calc(var(--space-xl) * 1.3);
}

.section-inner {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.04), rgba(255, 255, 255, 0.02));
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 28px;
  padding: clamp(1.4rem, 5vw, 2.5rem);
  box-shadow: var(--shadow-card);
}

.section-headline {
  display: grid;
  gap: 0.35rem;
  margin-bottom: var(--space-lg);
}

.eyebrow {
  font-size: 0.85rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: rgba(148, 163, 184, 0.85);
}

.section-title {
  font-size: clamp(1.75rem, 4vw, 2.4rem);
  font-weight: 800;
  letter-spacing: -0.02em;
  margin: 0;
}

.section-subtitle {
  color: rgba(226, 232, 240, 0.8);
  margin: 0;
}

/* Stack cards vertically */
.projects {
  display: flex;
  flex-direction: column;
  gap: 16px;
}

/* =========================
   TABLET (iPad)
   ========================= */
@media (min-width: 768px) {
  .section {
    padding: 3rem 0;
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
    padding: 4rem 0;
  }

  .projects {
    gap: 32px;
  }
}
</style>
