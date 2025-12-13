<!-- Each service card ----------------------->
<template>
  <div class="card">

    <!-- Emoji icon -->
    <div class="icon">{{ icon }}</div>

    <!-- Service title -->
    <h3 class="title">{{ title }}</h3>

    <!-- Service description -->
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
    }
  }
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
  .card {
    background: white;
    padding: 16px;
    border-radius: 12px;
    box-shadow: 0px 2px 6px rgba(0,0,0,0.06);
    margin-bottom: 16px;
  }

  .icon {
    font-size: 24px;
  }

  .title {
    font-weight: 600;
    margin-top: 8px;
  }

  .description {
    color: #555;
    margin-top: 8px;
    line-height: 1.4;
  }
</style>
