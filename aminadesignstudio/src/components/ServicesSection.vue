<!-- Wrapper for the services -->
<template>
  <section class="section container">
    <!-- Section title -->
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
        description="Visual systems that capture your brand’s unique story."
      />
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
  margin: 0;
}

.grid {
  display: grid;
  gap: 0.9rem;
}

@media (min-width: 768px) {
  .section {
    gap: 1.75rem;
  }

  .grid {
    grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
    gap: 1.1rem;
  }
}

@media (min-width: 75rem) {
  .section {
    padding: var(--space-2xl) 0;
  }

  .grid {
    gap: 1.2rem;
  }
}
</style>
