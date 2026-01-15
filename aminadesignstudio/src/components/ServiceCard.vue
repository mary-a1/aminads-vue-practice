<!-- Each service card ----------------------->
<template>
  <div class="card">
    <div class="icon-wrapper">
      <span class="icon">{{ icon }}</span>
    </div>

    <div class="text">
      <h3 class="title">{{ title }}</h3>
      <p class="description">{{ description }}</p>
    </div>

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
  background: linear-gradient(140deg, rgba(255, 255, 255, 0.06), rgba(255, 255, 255, 0.02));
  padding: 1.2rem 1.4rem;
  border-radius: 16px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  box-shadow: var(--shadow-card);
  display: grid;
  grid-template-columns: auto 1fr auto;
  gap: 1rem;
  align-items: center;
  transition: transform 0.25s ease, box-shadow 0.25s ease, border-color 0.25s ease;
}

/* Icon container */
.icon-wrapper {
  width: 2.75rem;
  height: 2.75rem;
  border-radius: 0.9rem;
  background: radial-gradient(circle at 20% 20%, rgba(168, 85, 247, 0.3), rgba(56, 189, 248, 0.25));
  border: 1px solid rgba(255, 255, 255, 0.12);
  display: flex;
  align-items: center;
  justify-content: center;
  box-shadow: 0 12px 30px rgba(0, 0, 0, 0.2);
}

/* Icon itself */
.icon {
  font-size: 1.2rem;
}

.text {
  display: grid;
  gap: 0.2rem;
}

/* Title */
.title {
  margin: 0;
  font-size: 1.05rem;
  font-weight: 700;
  line-height: 1.3;
}

/* Description */
.description {
  margin: 0;
  font-size: 0.95rem;
  color: rgba(226, 232, 240, 0.82);
  line-height: 1.6;
}

.chevron {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  width: 2.4rem;
  height: 2.4rem;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.06);
  border: 1px solid rgba(255, 255, 255, 0.12);
  color: #e5e7eb;
  font-weight: 700;
}

/* =========================
    INTERACTION (Desktop feel)
    ========================= */
@media (hover: hover) {
  .card:hover {
    transform: translateY(-4px);
    box-shadow: 0 18px 40px rgba(0, 0, 0, 0.3);
    border-color: rgba(168, 85, 247, 0.45);
  }
}

/* =========================
    TABLET
    ========================= */
@media (min-width: 768px) {
  .card {
    padding: 1.35rem 1.6rem;
  }

  .title {
    font-size: 1.15rem;
  }
}

/* =========================
    DESKTOP
    ========================= */
@media (min-width: 1200px) {
  .card {
    padding: 1.5rem 1.85rem;
  }

  .description {
    font-size: 1rem;
  }
}
</style>
