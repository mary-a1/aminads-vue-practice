<!-- The container for each project -->
<template>
  <div class="card">
    <div class="card-content">
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
  </div>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "ProjectCard",
  // Props allow the parent component to pass data down to this component
  props: {
    title: String,
    subtitle: String,
    description: String,
    url: String,
  },
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
/* =========================
   BASE (Mobile-first)
   ========================= */

.card {
  background: #fff;
  padding: 1.25rem; /* 20px */
  border-radius: 0.75rem; /* 12px */
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.06);
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.card-content {
  display: flex;
  flex-direction: column;
}

/* Title */
.title {
  font-size: 1.125rem; /* 18px */
  font-weight: 700;
  line-height: 1.3;
}

/* Subtitle */
.subtitle {
  margin-top: 0.25rem;
  font-size: 0.95rem;
  font-weight: 600;
  color: #6b46ff;
}

/* Description */
.description {
  margin-top: 0.75rem;
  font-size: 0.95rem;
  color: #555;
  line-height: 1.6;
}

/* Link */
.link {
  margin-top: 0.75rem;
  font-size: 0.9rem;
}

.link a {
  color: #6b46ff;
  text-decoration: none;
  border-bottom: 1px solid transparent;
  transition: border-color 0.2s ease;
}

.link a:hover {
  border-color: #6b46ff;
}

/* =========================
   INTERACTION (Desktop feel)
   ========================= */
@media (hover: hover) {
  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 10px 24px rgba(0, 0, 0, 0.08);
  }
}

/* =========================
   TABLET
   ========================= */
@media (min-width: 768px) {
  .card {
    padding: 1.5rem;
  }

  .title {
    font-size: 1.25rem;
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 1200px) {
  .card {
    padding: 1.75rem;
  }

  .description {
    font-size: 1rem;
  }
}
</style>
