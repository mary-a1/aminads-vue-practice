<!-- Footer wrapper -->
<template>
  <footer class="footer">
    <div class="footer-inner container">
      <!-- Copyright -->
      <div class="brand">
        <p class="eyebrow">Amina Design Co.</p>
        <p class="copyright">© 2024 All rights reserved.</p>
      </div>

      <!-- Simple link list -->
      <div class="links">
        <a href="#">Contact</a>
        <a href="#">Instagram</a>
        <a href="#">LinkedIn</a>
      </div>
    </div>
  </footer>
</template>

<script>
export default {
  name: "Footer",
};
</script>

<style scoped>
.footer {
  padding: 2rem 0 2.5rem;
  background: linear-gradient(180deg, rgba(255, 255, 255, 0.02), rgba(255, 255, 255, 0.04));
  border-top: 1px solid rgba(255, 255, 255, 0.06);
  margin-top: 2rem;
}

.footer-inner {
  display: grid;
  gap: 1rem;
  align-items: center;
  justify-content: space-between;
}

.brand {
  display: grid;
  gap: 0.3rem;
}

.eyebrow {
  margin: 0;
  font-size: 0.85rem;
  letter-spacing: 0.12em;
  text-transform: uppercase;
  color: rgba(148, 163, 184, 0.85);
}

.copyright {
  margin: 0;
  color: rgba(226, 232, 240, 0.8);
  font-size: 0.95rem;
}

.links {
  display: flex;
  justify-content: flex-start;
  gap: 16px;
}

.links a {
  text-decoration: none;
  color: rgba(226, 232, 240, 0.9);
  padding: 0.45rem 0.75rem;
  border-radius: 999px;
  border: 1px solid rgba(255, 255, 255, 0.08);
  background: rgba(255, 255, 255, 0.04);
}

@media (min-width: 768px) {
  .footer-inner {
    grid-template-columns: auto auto;
  }
}
</style>
