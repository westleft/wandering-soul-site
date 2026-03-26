<template>
  <div class="ws ws--contact">
    <main class="ws-main">
      <section class="ws-contact">
        <header class="ws-contact__header">
          <h1 class="ws-contact__title">聯絡我們</h1>
          <p class="ws-contact__note">
            如果你遇到使用問題、帳號相關需求，或想提供建議，歡迎透過以下方式聯絡「流浪靈魂」團隊。
          </p>
        </header>

        <div class="ws-contact__content">
          <section class="ws-contact__section">
            <h2>電子郵件聯絡</h2>
            <p>你可以直接寄信給我們，我們會盡快回覆。</p>
            <p class="ws-contact__email">
              <a href="mailto:service@wandering-soul.app">service@wandering-soul.app</a>
            </p>
          </section>

          <section class="ws-contact__section">
            <h2>聯絡表單</h2>
            <p>你也可以透過以下表單回報問題或提供建議：</p>
            <p class="ws-contact__form-link">
              <a
                href="https://docs.google.com/forms/d/e/1FAIpQLSfDtexKQoZBx4cbxl0loIVCqLEklEJ2V5OBd8lW-Pc6FMlNoQ/viewform"
                target="_blank"
                rel="noopener noreferrer"
              >
                前往流浪靈魂聯絡表單
              </a>
            </p>
          </section>
        </div>
      </section>
    </main>
  </div>
</template>

<script setup lang="ts">
</script>

<style scoped>
.ws {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  color: #e5e7eb;
  background-color: #192955;
}

.ws-main {
  flex: 1;
  display: flex;
  flex-direction: column;
  padding: 4rem 3.5rem 3.5rem;
}

.ws-contact {
  max-width: 800px;
  margin: 0 auto;
}

.ws-contact__header {
  margin-bottom: 2.5rem;
}

.ws-contact__title {
  font-size: clamp(2.2rem, 3vw, 2.6rem);
  font-weight: 700;
  letter-spacing: 0.12em;
  margin-bottom: 0.75rem;
}

.ws-contact__note {
  font-size: 0.95rem;
  color: #d1d5db;
  line-height: 1.7;
}

.ws-contact__content {
  display: flex;
  flex-direction: column;
  gap: 1.9rem;
  font-size: 0.98rem;
  line-height: 1.9;
}

.ws-contact__section h2 {
  font-size: 1.1rem;
  font-weight: 600;
  margin-bottom: 0.5rem;
  color: #e5e7eb;
}

.ws-contact__section p + p {
  margin-top: 0.6rem;
}

.ws-contact__email a,
.ws-contact__form-link a {
  color: #7dd3fc;
  text-decoration: none;
}

.ws-contact__email a:hover,
.ws-contact__form-link a:hover {
  text-decoration: underline;
}

@media (max-width: 960px) {
  .ws-main {
    padding-inline: 1.5rem;
  }
}

@media (max-width: 640px) {
  .ws-main {
    padding-inline: 1.25rem;
  }
}
</style>
