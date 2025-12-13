<!-- Simple location tag with an emoji wrapper -->
<template>
  <div class="location">
    📍 Toronto, Canada
  </div>
</template>

<!-- Options API format ----------------------------------->
<script>
  export default {
    name: "LocationTag"
  }
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
  .location {
    padding: 0 24px;
    margin-top: 16px;
    color: #777;
  }
</style>
