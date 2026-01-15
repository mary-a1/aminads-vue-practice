<!-- This is the main homepage. We assemble all our components here ----->
<template>
    <Navbar />
    <Hero />
    <FeaturedProjects />
    <StudioSection />
    <ServicesSection />
    <Footer />
</template>

<script>
// Import all section components manually
import Navbar from "../components/Navbar.vue";
import Hero from "../components/Hero.vue";
import LocationTag from "../components/LocationTag.vue";
import FeaturedProjects from "../components/FeaturedProjects.vue";
import StudioSection from "../components/StudioSection.vue";
import ServicesSection from "../components/ServicesSection.vue";
import Footer from "../components/Footer.vue";
import ContactSection from "@/components/ContactSection.vue";

export default {
  name: "HomeView",
  // Register imported components
  components: {
    Navbar,
    Hero,
    LocationTag,
    FeaturedProjects,
    StudioSection,
    ServicesSection,
    ContactSection,
    Footer,
  },
};
</script>
