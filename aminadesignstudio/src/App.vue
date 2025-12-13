<!-- router-view is where pages load. Since you only have one page (HomeView.vue),
 THIS tag is responsible for rendering your entire site.-->
<template>
  <router-view />
</template>

<script>
  export default {
    name: "App",
  };
</script>

<style>
  /* Global styles */
  /* You can add a global font, reset styles, etc. */

  body {
    margin: 0;
    font-family: system-ui, sans-serif;
    background: #fafafa;
  }

  /* Global layout container */
.container {
  width: 100%;
  padding-inline: 20px;
}

/* Tablet */
@media (min-width: 768px) {
  .container {
    padding-inline: 40px;
  }
}

/* Desktop */
@media (min-width: 1200px) {
  .container {
    max-width: 1100px;
    margin-inline: auto;
    padding-inline: 0;
  }
}

</style>

