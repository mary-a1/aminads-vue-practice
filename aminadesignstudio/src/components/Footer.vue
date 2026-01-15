<!-- Footer wrapper -->
<template>
  <footer class="footer">
    <div class="footer-inner container">
      <!-- Brand block -->
      <div class="brand">
        <div class="brand-row">
          <img
            src="/src/assets/images/logo.png"
            alt="Amina Design Co."
            class="logo"
          />
          <div class="brand-text">
            <p class="brand-name">Amina Design Co.</p>
            <p class="copyright">© 2026 All rights reserved.</p>
          </div>
        </div>
      </div>

      <!-- Links -->
      <div class="links">
        <a href="#contact">Contact</a>
        <a href="https://instagram.com" target="_blank">Instagram</a>
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
.logo {
  height: 2.4rem;
  width: auto;
  filter: drop-shadow(0 6px 18px rgba(168, 85, 247, 0.35));
}

.brand-row {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.brand-text {
  display: grid;
  gap: 0.15rem;
}

.brand-name {
  margin: 0;
  font-size: 0.9rem;
  font-weight: 700;
  letter-spacing: 0.02em;
  color: #e5e7eb;
}

@media (min-width: 768px) {
  .footer-inner {
    grid-template-columns: auto auto;
  }
}
</style>
