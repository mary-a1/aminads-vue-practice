<!-- The container for each project -->
<template>
  <div class="card">
    <!-- Title -->
    <h3 class="title">{{ title }}</h3>

    <!-- Subtitle (purple text) -->
    <p class="subtitle">{{ subtitle }}</p>

    <!-- Description of the project -->
    <p class="description">{{ description }}</p>

    <!-- Live link -->
    <p class="link">
      <strong>Live:</strong>
      <!--
        :href binds the value dynamically using the `url` prop
      -->
      <a :href="url" target="_blank">{{ url }}</a>
    </p>
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
  .card {
    background: white;
    padding: 16px;
    border-radius: 12px;
    box-shadow: 0px 2px 6px rgba(0, 0, 0, 0.06);
    margin-bottom: 16px;
  }
  .title {
    font-weight: 600;
    font-size: 18px;
  }
  .subtitle {
    color: #6b46ff;
    margin-top: 4px;
  }
  .description {
    color: #555;
    margin-top: 12px;
  }
  .link {
    margin-top: 12px;
  }
</style>
