<!-- The container for each project -->
<template>
  <article class="project-card">
    <div class="project-grid">

      <!-- TEXT -->
      <div class="project-text">
        <h3 class="title">{{ title }}</h3>
        <p class="subtitle">{{ subtitle }}</p>
        <p class="description">{{ description }}</p>

        <p class="link">
          <strong>Live:</strong>
          <a :href="url" target="_blank" rel="noopener noreferrer">
            {{ url }}
          </a>
        </p>
      </div>

      <!-- LOGO -->
      <div class="project-logo">
        <img :src="logo" :alt="title + ' logo'" />
      </div>

    </div>
  </article>
</template>


<!-- Options API format ----------------------------------->
<script>
export default {
  name: "ProjectCard",
  props: {
    title: String,
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
    background: white;
    border-radius: var(--radius-lg);
    padding: var(--space-xl);
    box-shadow: 0 1rem 2.5rem rgba(0,0,0,0.06);
    transition: transform 0.3s ease, box-shadow 0.3s ease;
  }

  .project-card:hover {
    transform: translateY(-4px);
    box-shadow: 0 1.5rem 3rem rgba(0,0,0,0.08);
  }

  .project-grid {
    display: grid;
    grid-template-columns: 1fr auto;
    gap: var(--space-xl);
    align-items: center;
  }

  /* TEXT */
  .title {
    font-size: var(--text-xl);
    font-weight: 700;
    color: var(--color-primary);
  }

  .subtitle {
    margin-top: var(--space-xs);
    color: var(--color-accent);
    font-size: var(--text-base);
  }

  .description {
    margin-top: var(--space-md);
    color: #555;
    line-height: 1.6;
    max-width: 52ch;
  }

  .link {
    margin-top: var(--space-md);
    font-size: var(--text-sm);
  }

  /* LOGO */
  .project-logo {
    width: 5.5rem;
    height: 5.5rem;
    display: flex;
    align-items: center;
    justify-content: center;
  }

  .project-logo img {
    max-width: 100%;
    max-height: 100%;
    object-fit: contain;
    opacity: 0.85;
  }

  /* ===== MOBILE ===== */
  @media (max-width: 48rem) {
    .project-grid {
      grid-template-columns: 1fr;
      text-align: left;
    }

    .project-logo {
      order: -1;
      margin-bottom: var(--space-md);
      width: 4.5rem;
      height: 4.5rem;
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
