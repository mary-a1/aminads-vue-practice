<!-- Main hero section wrapper -------------------->
<template>
  <section class="hero">
    <div class="hero-inner container">
      <!-- Small uppercase tagline -->
      <p class="tagline">WEB & DIGITAL PRODUCT DESIGN STUDIO</p>

      <!-- Main heading text <br> creates line breaks just like in your design -->
      <h1 class="title">
        Building <br />
        Modern <br />
        <span class="highlight">Digital</span> <br />
        Experiences
      </h1>

      <!-- Supporting description text -->
      <p class="description">
        From fintech platforms to e-commerce brands — we design and build exceptional websites and
        digital products.
      </p>

      <!-- Buttons group -->
      <div class="buttons">
        <button class="primary">Start a Project</button>
        <button class="secondary">View Our Work</button>
      </div>
    </div>
  </section>
</template>

<!-- Options API format ----------------------------------->
<script>
export default {
  name: "Hero",
};
</script>

<!-- Scoped CSS = styles apply only to this component ----------------------->
<style scoped>
  /* SECTION PADDING */
  .hero {
    padding: 24px;
  }

  /* TAGLINE STYLING */
  .tagline {
    color: #6b46ff;
    font-size: 12px;
    letter-spacing: 1px;
  }

  /* MAIN HEADING STYLING */
  .title {
    margin-top: 12px;
    font-size: 38px;
    font-weight: 800;
    line-height: 1.1; /* tighter line spacing */
  }

  /* COLORED WORD */
  .highlight {
    color: #7c3aed;
  }

  /* PARAGRAPH TEXT */
  .description {
    margin-top: 16px;
    color: #666;
    line-height: 1.5;
  }

  /* BUTTON LAYOUT */
  .buttons {
    margin-top: 24px;
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  /* BLACK BUTTON */
  .primary {
    background: #111;
    padding: 14px;
    color: white;
    border-radius: 8px;
  }

  /* OUTLINE BUTTON */
  .secondary {
    padding: 14px;
    border-radius: 8px;
    border: 1px solid #ddd;
    background: white;
  }

  /* =========================
    TABLET (iPad)
    ========================= */
  @media (min-width: 768px) {
    .hero {
      padding: 64px 40px;
    }
  }

  /* =========================
    DESKTOP
    ========================= */
  @media (min-width: 1200px) {
    .hero {
      padding: 80px 0;
    }

    .hero-inner {
      max-width: 720px;
      margin: 0 auto;
      text-align: center;
    }

    .title {
      font-size: 56px;
    }

    .description {
      font-size: 18px;
    }

    .buttons {
      flex-direction: row;
      justify-content: center;
    }
  }
</style>
