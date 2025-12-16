<!-- Each service card ----------------------->
<template>
  <div class="card">
    <div class="icon-wrapper">
      <span class="icon">{{ icon }}</span>
    </div>

    <h3 class="title">{{ title }}</h3>

    <p class="description">{{ description }}</p>
  </div>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "ServiceCard",

  // Props = data passed from ServicesSection to each card
  props: {
    icon: String,
    title: String,
    description: String,
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

/* Icon container */
.icon-wrapper {
  width: 2.5rem;
  height: 2.5rem;
  border-radius: 0.5rem;
  background: rgba(124, 58, 237, 0.08);
  display: flex;
  align-items: center;
  justify-content: center;
  margin-bottom: 0.25rem;
}

/* Icon itself */
.icon {
  font-size: 1.25rem;
}

/* Title */
.title {
  margin-top: 0.5rem;
  font-size: 1.1rem;
  font-weight: 700;
  line-height: 1.3;
}

/* Description */
.description {
  margin-top: 0.5rem;
  font-size: 0.95rem;
  color: #555;
  line-height: 1.6;
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
    font-size: 1.2rem;
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
