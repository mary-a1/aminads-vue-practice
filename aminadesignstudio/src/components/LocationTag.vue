<template>
  <div class="location">
    📍 Toronto, Canada
  </div>
</template>

<script>
export default {
  name: "LocationTag"
}
</script>

<style scoped>
/* Mobile */
.location {
  margin-top: 16px;
  padding: 0 24px;
  color: #777;
  font-size: 14px;
}

/* Tablet */
@media (min-width: 768px) {
  .location {
    padding: 0;
    margin-top: 24px;
  }
}

/* Desktop */
@media (min-width: 1200px) {
  .location {
    margin-top: 32px;
    text-align: center;
  }
}
</style>
