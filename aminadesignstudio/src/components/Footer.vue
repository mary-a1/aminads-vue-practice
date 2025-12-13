<!-- Footer wrapper -->
<template>
  <footer class="footer">

    <!-- Copyright -->
    <p>© 2024 Amina Design Co. All rights reserved.</p>

    <!-- Simple link list -->
    <div class="links">
      <a href="#">Contact</a>
      <a href="#">Instagram</a>
      <a href="#">LinkedIn</a>
    </div>

  </footer>
</template>

<script>
  export default {
    name: "Footer"
  }
</script>

<style scoped>
  .footer {
    padding: 32px 24px;
    text-align: center;
    color: #666;
    font-size: 14px;
  }

  .links {
    display: flex;
    justify-content: center;
    gap: 20px;
    margin-top: 12px;
  }

  .links a {
    text-decoration: underline;
  }
</style>
