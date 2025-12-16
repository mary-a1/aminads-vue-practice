<template>
  <div class="location">
    <span class="dot" aria-hidden="true"></span>
    <span class="text"> Toronto, Canada</span>
  </div>
</template>

<script>
export default {
  name: "LocationTag"
}
</script>

<style scoped>
/* =========================
   BASE (Mobile-first)
   ========================= */
.location {
  margin-top: var(--space-lg);
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;

  font-size: var(--text-sm);
  font-weight: 500;
  color: var(--color-text-muted);
}

/* Presence dot */
.dot {
  width: 0.5rem;
  height: 0.5rem;
  border-radius: 50%;
  background: var(--color-primary);
  box-shadow: 0 0 0 4px rgba(124, 58, 237, 0.12);
}

/* =========================
   TABLET
   ========================= */
@media (min-width: 48rem) {
  .location {
    margin-top: var(--space-xl);
  }
}

/* =========================
   DESKTOP
   ========================= */
@media (min-width: 75rem) {
  .location {
    margin-top: calc(var(--space-xl) * 1.25);
    margin-inline: auto;
  }
}
</style>
