<!-- The container for each project -->
<template>
  <article class="project-card">
    <!-- <div class="card-top">
      <div class="project-logo">
        <span class="logo-glow" aria-hidden="true"></span>
        <img :src="logo" :alt="title + ' logo'" />
      </div>

      <div class="meta-tags">
        <span class="pill pill-primary">{{ primaryTag }}</span>
        <span class="pill pill-soft">{{ secondaryTag }}</span>
      </div>
    </div> -->
    <div class="card-top">
      <div class="project-header">
        <div class="project-logo">
          <img :src="logo" :alt="title + ' logo'" class="project-logo" />
        </div>

        <div class="project-heading">
          <h3 class="title">{{ title }}</h3>
        </div>
      </div>

      <div class="meta-tags">
        <span class="pill pill-primary">{{ primaryTag }}</span>
        <span class="pill pill-soft">{{ secondaryTag }}</span>
      </div>
    </div>

    <div class="project-body">
      <!-- TEXT -->
      <div class="project-text">
        <p class="eyebrow">Case study</p>

        <p class="subtitle">{{ subtitle }}</p>
        <p class="description">{{ description }}</p>
      </div>

      <a class="cta" :href="url" target="_blank" rel="noopener noreferrer">
        <span>View live experience</span>
        <span aria-hidden="true">→</span>
      </a>
    </div>
  </article>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "ProjectCard",
  props: {
    title: String,
    primaryTag: String,
    secondaryTag: String,
    subtitle: String,
    description: String,
    url: String,
    logo: String,
  },
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* ===== BASE ===== */
.project-card {
  background: linear-gradient(145deg, #0f172a, #111827 35%, #0b1020);
  border: 1px solid rgba(255, 255, 255, 0.06);
  border-radius: var(--radius-lg);
  padding: var(--space-xl);
  position: relative;
  overflow: hidden;
  box-shadow: 0 20px 45px rgba(0, 0, 0, 0.24);
  transition: transform 0.3s ease, box-shadow 0.3s ease, border-color 0.3s ease;
}

.project-card::after {
  content: "";
  position: absolute;
  inset: -30% auto auto 60%;
  width: 340px;
  height: 340px;
  background: radial-gradient(circle, rgba(124, 58, 237, 0.18), transparent 55%);
  filter: blur(12px);
  pointer-events: none;
  opacity: 0.8;
}

.project-card:hover {
  transform: translateY(-6px);
  border-color: rgba(124, 58, 237, 0.35);
  box-shadow: 0 30px 65px rgba(0, 0, 0, 0.3);
}

.card-top {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
  gap: var(--space-md);
}

.meta-tags {
  display: flex;
  gap: 0.5rem;
  flex-wrap: wrap;
  justify-content: flex-end;
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.35rem 0.7rem;
  border-radius: 999px;
  font-size: var(--text-xs);
  letter-spacing: 0.01em;
  border: 1px solid rgba(255, 255, 255, 0.08);
  color: rgba(255, 255, 255, 0.82);
  background: rgba(255, 255, 255, 0.04);
}

.pill-primary {
  border-color: rgba(124, 58, 237, 0.4);
  background: linear-gradient(135deg, rgba(124, 58, 237, 0.22), rgba(56, 189, 248, 0.18));
  color: #f5f3ff;
}

.pill-soft {
  color: rgba(255, 255, 255, 0.74);
}

.project-body {
  display: grid;
  grid-template-columns: 1fr auto;
  gap: var(--space-lg);
  align-items: center;
}

.eyebrow {
  font-size: var(--text-xs);
  text-transform: uppercase;
  letter-spacing: 0.15em;
  color: rgba(255, 255, 255, 0.64);
  margin-bottom: var(--space-xs);
}

/* TEXT */
.title {
  font-size: var(--text-xl);
  font-weight: 700;
  color: #f8fafc;
}

.subtitle {
  margin-top: var(--space-xs);
  color: rgba(167, 139, 250, 0.95);
  font-size: var(--text-base);
}

.description {
  margin-top: var(--space-md);
  color: rgba(226, 232, 240, 0.86);
  line-height: 1.65;
  max-width: 60ch;
}

.cta {
  justify-self: flex-start;
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  padding: 0.65rem 1rem;
  border-radius: 0.9rem;
  color: #0f172a;
  font-weight: 700;
  background: linear-gradient(135deg, #a855f7, #60a5fa);
  box-shadow: 0 10px 25px rgba(96, 165, 250, 0.35);
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.cta:hover {
  transform: translateY(-2px);
  box-shadow: 0 16px 35px rgba(96, 165, 250, 0.45);
}

/* LOGO */

.project-logo {
  width: 5rem;
  height: 5rem;
  border-radius: 0.9rem;
  display: grid;
  place-items: center;
  flex-shrink: 0;
}

.project-logo img {
  max-width: 65%;
  max-height: 65%;
  object-fit: contain;
  filter: brightness(1.1);
}

.project-header {
  display: flex;
  align-items: center;
  gap: 0.9rem;
}

.project-heading {
  display: flex;
  flex-direction: column;
}

.logo-glow {
  position: absolute;
  inset: -40% auto auto -35%;
  width: 140%;
  height: 140%;
  background: radial-gradient(circle at 20% 20%, rgba(96, 165, 250, 0.35), transparent 55%);
  opacity: 0.85;
  filter: blur(4px);
}

/* ===== MOBILE ===== */
@media (max-width: 48rem) {
  .project-body {
    grid-template-columns: 1fr;
    gap: var(--space-md);
  }

  .card-top {
    flex-direction: column;
    align-items: flex-start;
  }

  .meta-tags {
    justify-content: flex-start;
  }
}

/* ===== DESKTOP ===== */
@media (min-width: 75rem) {
  .project-card {
    padding: var(--space-2xl);
  }

  .title {
    font-size: var(--text-2xl);
  }
}
</style>
