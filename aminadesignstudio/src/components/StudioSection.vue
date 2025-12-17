<!-- Wrapper for the entire studio/about section ------>
<template>
  <section class="studio container">
    <div class="studio-card">
      <div class="heading">
        <p class="eyebrow">About the practice</p>
        <h2 class="title">The Studio</h2>
        <p class="subtitle">A nimble, founder-led design studio shaping modern digital brands.</p>
      </div>

      <p class="body">
        Amina Design Co. is a Toronto-based web and digital product design studio
        specializing in crafting exceptional digital experiences for modern brands.

        <br /><br />

        Our approach combines strategic thinking, beautiful design, and robust development to
        deliver solutions that scale.

        <br /><br />

        Whether you're launching a new platform, refreshing your digital presence, or building a
        product from the ground up, we bring the expertise and attention to detail needed to bring
        your vision to life.
      </p>
    </div>
  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "StudioSection",
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
.studio {
  padding: clamp(1.75rem, 6vw, 3.25rem) 0;
}

.studio-card {
  background: linear-gradient(160deg, rgba(255, 255, 255, 0.05), rgba(255, 255, 255, 0.02));
  border-radius: 28px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  padding: clamp(1.4rem, 4vw, 2.6rem);
  box-shadow: var(--shadow-card);
  backdrop-filter: blur(12px);
}

.heading {
  display: grid;
  gap: 0.45rem;
  margin-bottom: var(--space-md);
}

.eyebrow {
  font-size: 0.85rem;
  letter-spacing: 0.16em;
  text-transform: uppercase;
  color: rgba(148, 163, 184, 0.85);
  margin: 0;
}

.title {
  font-size: clamp(1.75rem, 4vw, 2.4rem);
  font-weight: 800;
  margin: 0;
}

.subtitle {
  color: rgba(226, 232, 240, 0.8);
  margin: 0;
}

.body {
  color: rgba(226, 232, 240, 0.86);
  line-height: 1.7;
  font-size: 1rem;
  margin: 0;
}

@media (min-width: 75rem) {
  .studio {
    padding: var(--space-2xl) 0;
  }

  .studio-card {
    padding: 3rem;
    display: grid;
    grid-template-columns: 1.2fr 1.8fr;
    gap: 2rem;
    align-items: start;
  }

  .heading {
    margin-bottom: 0;
  }
}
</style>
