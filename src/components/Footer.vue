<template>
  <footer class="footer">
    <div class="footer-left">
      <span>© 2026 Wandering Soul. 保留所有權利。</span>
    </div>
    <div class="footer-links">
      <a id="privacy" href="#privacy">隱私政策</a>
      <a id="terms" href="#terms">服務條款</a>
      <a href="#contact">聯繫我們</a>
    </div>
  </footer>
</template>

<style scoped>
.footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.5rem 3.5rem 2rem;
  font-size: 0.8rem;
  color: #6b7280;
  border-top: 1px solid rgba(31, 41, 55, 0.9);
  background: radial-gradient(circle at top, #020617 0, #000 70%);
}

.footer-links {
  display: flex;
  gap: 1.5rem;
}

.footer-links a {
  color: inherit;
  text-decoration: none;
}

.footer-links a:hover {
  color: #e5e7eb;
}
</style>