<!-- Main hero section wrapper -------------------->
<template>
  <section id="hero" class="hero">
    <div class="hero-inner container">
      <div class="hero-card">
        <div class="pill-row">
          <span class="pill pill-primary">Digital Product & UX Studio</span>
          <span class="pill pill-soft">Accepting new builds</span>
        </div>

        <h1 class="title">Designing and building launch-ready digital products.</h1>

        <p class="description">
          We help fintech, SaaS, e-commerce, and growing businesses design and improve digital
          experiences—from full platforms to focused websites and workflows.
        </p>

        <div class="buttons">
          <button class="primary" @click="scrollToContact" data-focus="project">Start a project</button>
          <button class="secondary" @click="scrollToProjects">See the portfolio</button>
        </div>

        <div class="stats">
          <div class="stat">
            <span class="label">Platforms shipped</span>
            <span class="value">3+</span>
          </div>
          <div class="stat">
            <span class="label">Avg. launch time</span>
            <span class="value">6 weeks</span>
          </div>
          <div class="stat">
            <span class="label">Locations</span>
            <span class="value">Remote · Toronto</span>
          </div>
        </div>

        <LocationTag />
      </div>
    </div>
  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
import LocationTag from "./LocationTag.vue";

export default {
  name: "Hero",
  components: {
    LocationTag,
  },
  methods:{
    scrollToContact() {
      const el = document.getElementById("contact");
      if (!el) return;

      el.scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    },
    scrollToProjects() {
      const el = document.getElementById("projects");
      if (!el) return;

      el.scrollIntoView({
        behavior: "smooth",
        block: "start",
      });
    },
  }

};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
.hero {
  position: relative;
  padding-block: calc(var(--space-xl) * 1.3);
  overflow: hidden;
}

.hero::before {
  content: "";
  position: absolute;
  inset: -20% auto auto -30%;
  width: 32rem;
  height: 32rem;
  background: radial-gradient(circle, rgba(168, 85, 247, 0.12), transparent 60%);
  filter: blur(10px);
}

.hero::after {
  content: "";
  position: absolute;
  inset: -15% -30% auto auto;
  width: 28rem;
  height: 28rem;
  background: radial-gradient(circle, rgba(56, 189, 248, 0.12), transparent 60%);
  filter: blur(12px);
}

.hero-inner {
  position: relative;
  z-index: 1;
}

.hero-card {
  background: linear-gradient(145deg, rgba(255, 255, 255, 0.06), rgba(255, 255, 255, 0.02));
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 28px;
  padding: clamp(1.4rem, 4vw, 2.4rem);
  box-shadow: var(--shadow-card);
  backdrop-filter: blur(16px);
}

.pill-row {
  display: flex;
  gap: 0.65rem;
  flex-wrap: wrap;
  margin-bottom: var(--space-md);
}

.pill {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.5rem 0.85rem;
  border-radius: 999px;
  border: 1px solid rgba(255, 255, 255, 0.12);
  color: rgba(226, 232, 240, 0.9);
  background: rgba(255, 255, 255, 0.04);
  font-size: 0.85rem;
}

.pill-primary {
  background: linear-gradient(135deg, rgba(168, 85, 247, 0.25), rgba(56, 189, 248, 0.22));
  color: #f8fafc;
  border-color: rgba(168, 85, 247, 0.35);
}

.pill-soft {
  color: rgba(226, 232, 240, 0.8);
}

.title {
  font-size: clamp(2rem, 5vw, 3.6rem);
  font-weight: 900;
  line-height: 1.08;
  margin: 0;
}

.description {
  margin-top: var(--space-md);
  font-size: 1.05rem;
  color: rgba(226, 232, 240, 0.82);
  max-width: 44rem;
}

.buttons {
  margin-top: var(--space-lg);
  display: flex;
  gap: 0.75rem;
  flex-wrap: wrap;
}

.primary {
  background: linear-gradient(135deg, #a855f7, #38bdf8);
  color: #0f172a;
  padding: 0.95rem 1.6rem;
  border-radius: 14px;
  font-size: var(--text-base);
  font-weight: 700;
  border: none;
  box-shadow: 0 16px 35px rgba(56, 189, 248, 0.35);
}

.secondary {
  background: rgba(255, 255, 255, 0.04);
  border: 1px solid rgba(255, 255, 255, 0.12);
  color: rgba(226, 232, 240, 0.88);
  padding: 0.95rem 1.4rem;
  border-radius: 14px;
  font-size: var(--text-base);
}

.stats {
  margin-top: var(--space-lg);
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(150px, 1fr));
  gap: 0.85rem;
}

.stat {
  padding: 0.85rem 1rem;
  border-radius: 14px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  background: rgba(255, 255, 255, 0.03);
}

.label {
  display: block;
  font-size: 0.85rem;
  color: rgba(148, 163, 184, 0.9);
}

.value {
  display: block;
  margin-top: 0.3rem;
  font-weight: 800;
  font-size: 1.4rem;
}

@media (min-width: 48rem) {
  .hero-card {
    padding: 2.4rem 2.8rem;
  }

  .description {
    font-size: 1.1rem;
  }
}

@media (min-width: 75rem) {
  .hero {
    padding-block: var(--space-2xl);
  }

  .hero-inner {
    max-width: 68rem;
  }
}
</style>
