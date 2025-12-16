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

:root {
  /* Type scale */
  --text-xs: 0.75rem;   /* 12px */
  --text-sm: 0.875rem; /* 14px */
  --text-base: 1rem;   /* 16px */
  --text-lg: 1.125rem; /* 18px */
  --text-xl: 1.5rem;   /* 24px */
  --text-2xl: 2rem;    /* 32px */
  --text-3xl: 3rem;    /* 48px */

  /* Spacing scale */
  --space-xs: 0.5rem;
  --space-sm: 0.75rem;
  --space-md: 1rem;
  --space-lg: 1.5rem;
  --space-xl: 2.5rem;
  --space-2xl: 4rem;

  /* Radius */
  --radius-sm: 0.5rem;
  --radius-md: 0.75rem;
  --radius-lg: 1rem;
}

</style>

