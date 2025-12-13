<!-- Wrapper for the services -->
<template>
  <section class="section">
    <!-- Section title -->
    <h2 class="title">Services</h2>

    <!-- Subtitle -->
    <p class="subtitle">Comprehensive design and development for digital products</p>

    <!--
      Using the same card structure repeatedly
      Making the component reusable
    -->
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
    padding: 24px;
  }

  .title {
    font-size: 20px;
    font-weight: 700;
  }

  .subtitle {
    color: #666;
    margin-top: 4px;
    margin-bottom: 16px;
    font-size: 14px;
  }
</style>
