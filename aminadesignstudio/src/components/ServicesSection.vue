<!-- Wrapper for the services -->
<template>
  <section id="services" class="section">
    <!-- Section title -->
    <div class="container">
      <div class="services-card">
        <div class="heading">
          <p class="eyebrow">Capabilities</p>
          <h2 class="title">Services</h2>
          <p class="subtitle">Comprehensive design and development for digital products</p>
        </div>
        <div class="grid">
          <ServiceCard
            icon="🧠"
            title="Design Systems"
            description="Scalable, accessible design systems that power your product growth."
          />

          <ServiceCard
            icon="💻"
            title="Web Development"
            description="Fast, modern websites built with cutting-edge technologies."
          />

          <ServiceCard
            icon="📱"
            title="Digital Products"
            description="End-to-end product design from concept to launch."
          />

          <ServiceCard
            icon="🛒"
            title="E-commerce Solutions"
            description="Custom Shopify stores and product experiences that convert."
          />

          <ServiceCard
            icon="🎛"
            title="UX/UI Design"
            description="User-centered design that balances beauty with functionality."
          />

          <ServiceCard
            icon="✨"
            title="Brand Identity"
            description="Visual systems that capture your brand's unique story."
          />
        </div>
      </div>
    </div>
  </section>
</template>

<script>
// Import the child component
import ServiceCard from "./ServiceCard.vue";

export default {
  name: "ServicesSection",

  // Register child component
  components: {
    ServiceCard,
  },
};
</script>

<style scoped>
.section {
  padding: clamp(1.5rem, 6vw, 3rem) 0;
  display: grid;
  gap: 1.4rem;
}

.heading {
  display: grid;
  gap: 0.35rem;
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
  color: rgba(226, 232, 240, 0.78);
  padding: 10 0 0 10;
}

.grid {
  display: grid;
  gap: 0.9rem;
}
.services-card {
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.04), rgba(255, 255, 255, 0.02));
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 28px;
  padding: clamp(1.4rem, 5vw, 2.5rem);
  box-shadow: var(--shadow-card);
}
@media (min-width: 768px) {
  .section {
    gap: 1.75rem;
  }

  .grid {
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1.1rem;
  }
}

@media (min-width: 75rem) {
  .section {
    padding: var(--space-2xl) 0;
  }

  .grid {
    max-width: 68rem;
    margin-inline: auto;
  }
}
</style>
