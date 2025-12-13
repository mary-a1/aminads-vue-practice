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
        />

        <ProjectCard
          title="Maalin Active"
          subtitle="E-commerce brand & product experience"
          description="Shopify storefront, product experience, and brand system."
          url="https://maalinactive.com"
        />

        <ProjectCard
          title="Nasriina Studio"
          subtitle="Creative portfolio & digital operations"
          description="Website, LinkedIn, pricing system, and digital portfolio."
          url="#"
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
  font-size: 20px;
  font-weight: 700;
  margin-bottom: 16px;
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

