<template>
  <div class="ws">
    <main class="ws-main" id="top">
      <section class="ws-hero">
        <img src="../assets/icon.png" alt="流浪靈魂" class="ws-hero__image">
        <div class="ws-hero__content">
          <h1 class="ws-hero__title">流浪靈魂</h1>
          <p class="ws-hero__tagline">以缺點為主題的交友軟體</p>
          <div class="ws-hero__stores">
            <button class="store store--apple" type="button">

              <img src="../assets/app-store.png" alt="App Store" class="store__icon-image">
              <span class="store__text">
                <span class="store__label">立即下載 </span>
                <span class="store__brand">App Store</span>
              </span>
            </button>
            <button class="store store--google store-disabled" type="button" disabled>
              <img src="../assets/google-play.png" alt="Google Play" class="store__icon-image">
              <span class="store__text">
                <span class="store__label">尚未開放</span>
                <span class="store__brand">Google Play</span>
              </span>
            </button>
          </div>
        </div>
      </section>
    </main>

    <footer class="ws-footer">
      <div class="ws-footer__left">
        <span>© 2026 Wandering Soul. 保留所有權利。</span>
      </div>
      <div class="ws-footer__center">
        <a id="privacy" href="#privacy">隱私政策</a>
        <a id="terms" href="#terms">服務條款</a>
        <a href="#contact">聯繫我們</a>
      </div>
    </footer>
  </div>
</template>

<style scoped>
.ws {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  color: #e5e7eb;
  font-family: system-ui, -apple-system, BlinkMacSystemFont, 'SF Pro Text', sans-serif;
  background-color: #192955;
}

.store-disabled {
  opacity: 0.5;
  cursor: not-allowed;
  pointer-events: none;
  background-color: #192955;
  border-color: #192955;
  color: #9ca3af;
  box-shadow: none;
  transform: none;
  transition: none;
}

.store__icon-image {
  width: 32px;
}

.ws-hero__image {
  width: 20%;
}


.ws-main {
  flex: 1;
  display: flex;
  flex-direction: column;
  padding: 4rem 3.5rem 3.5rem;
  gap: 7rem;
}

.ws-hero {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  gap: 3.5rem;
  padding-top: 2rem;
}

.ws-hero__visual {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  padding: 4rem 2rem;
}

.ws-hero__orb {
  width: min(320px, 40vw);
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  position: relative;
  background:
    radial-gradient(circle at 32% 20%, #f9fafb 0, #e5e7eb 18%, transparent 52%),
    radial-gradient(circle at 45% 38%, #a855f7 0, #7c3aed 40%, #1f2937 82%);
  box-shadow:
    0 0 80px rgba(168, 85, 247, 0.9),
    0 0 180px rgba(59, 130, 246, 0.7),
    0 0 260px rgba(15, 23, 42, 0.95);
}

.ws-hero__orb::before {
  content: '';
  position: absolute;
  inset: 14%;
  border-radius: inherit;
  background: radial-gradient(circle at 30% 20%, rgba(248, 250, 252, 0.4), transparent 60%);
  mix-blend-mode: screen;
}

.ws-hero__orb::after {
  content: '';
  position: absolute;
  inset: -14%;
  border-radius: inherit;
  background: radial-gradient(circle, rgba(59, 130, 246, 0.18), transparent 70%);
  filter: blur(6px);
}

.ws-hero__content {
  display: flex;
  flex-direction: column;
  gap: 1.75rem;
}

.ws-hero__title {
  font-size: clamp(3rem, 4.2vw, 3.6rem);
  letter-spacing: 0.16em;
  font-weight: 700;
  text-align: center;
}

.ws-hero__tagline {
  font-size: 1rem;
  color: #9ca3af;
  text-align: center;
}

.ws-hero__stores {
  display: flex;
  flex-wrap: wrap;
  gap: 1rem;
  margin-top: 0.5rem;
}

.store {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  padding: 0.65rem 1.3rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.5);
  background: rgba(15, 23, 42, 0.95);
  color: #f9fafb;
  cursor: pointer;
  box-shadow: 0 14px 30px rgba(15, 23, 42, 0.95);
  transition:
    transform 120ms ease-out,
    box-shadow 120ms ease-out,
    border-color 120ms ease-out,
    background 120ms ease-out;
}

.store:hover {
  transform: translateY(-1px);
  border-color: rgba(248, 250, 252, 0.9);
  background: #020617;
}

.store__icon {
  width: 1.9rem;
  height: 1.9rem;
  border-radius: 0.7rem;
  display: inline-block;
  background: radial-gradient(circle at 30% 20%, #ffffff, #d1d5db 40%, #020617 95%);
}

.store__icon--google {
  background:
    conic-gradient(from 210deg, #22c55e, #ea580c, #facc15, #3b82f6, #22c55e);
}

.store__text {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  line-height: 1.1;
}

.store__label {
  font-size: 0.6rem;
  text-transform: uppercase;
  color: #9ca3af;
  padding-bottom: 4px;
}

.store__brand {
  font-size: 0.95rem;
  font-weight: 600;
}

.ws-eyebrow {
  font-size: 0.8rem;
  letter-spacing: 0.18em;
  text-transform: uppercase;
  color: #64748b;
  margin-bottom: 0.75rem;
}

.ws-phone {
  width: min(320px, 60vw);
  aspect-ratio: 9 / 19;
  border-radius: 2rem;
  padding: 0.4rem;
  background: radial-gradient(circle at top, #6d28d9, #020617 60%);
  box-shadow:
    0 36px 120px rgba(15, 23, 42, 1),
    0 0 80px rgba(59, 130, 246, 0.6);
  display: flex;
  align-items: stretch;
}

.ws-phone__inner {
  flex: 1;
  border-radius: 1.7rem;
  padding: 1.4rem 1.2rem;
  background: radial-gradient(circle at top, #020617, #020617 60%, #020617 100%);
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 1.2rem;
  position: relative;
}

.ws-phone__orb {
  width: 68%;
  aspect-ratio: 1 / 1;
  border-radius: 999px;
  background:
    radial-gradient(circle at 32% 20%, #f9fafb 0, #e5e7eb 18%, transparent 55%),
    radial-gradient(circle at 45% 40%, #a855f7 0, #7c3aed 40%, #020617 88%);
  box-shadow:
    0 0 40px rgba(168, 85, 247, 0.85),
    0 0 90px rgba(59, 130, 246, 0.8);
}

.ws-phone__id {
  font-size: 0.7rem;
  letter-spacing: 0.22em;
  color: #6b7280;
}

.ws-phone__chips {
  display: flex;
  flex-wrap: wrap;
  gap: 0.4rem;
  justify-content: center;
}

.ws-chip {
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.7);
  padding: 0.25rem 0.7rem;
  font-size: 0.7rem;
  color: #e5e7eb;
  background: rgba(15, 23, 42, 0.9);
}

.ws-chip--primary {
  border-color: transparent;
  background: linear-gradient(to right, #a855f7, #22d3ee);
  color: #020617;
}

.ws-footer {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.5rem 3.5rem 2rem;
  font-size: 0.8rem;
  color: #6b7280;
  border-top: 1px solid rgba(31, 41, 55, 0.9);
  background: radial-gradient(circle at top, #020617 0, #000 70%);
}

.ws-footer__center {
  display: flex;
  gap: 1.5rem;
}

.ws-footer__center a {
  color: inherit;
  text-decoration: none;
}

.ws-footer__center a:hover {
  color: #e5e7eb;
}

.ws-social {
  width: 2rem;
  height: 2rem;
  border-radius: 999px;
  border: 1px solid rgba(55, 65, 81, 0.9);
  background: #020617;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  color: #9ca3af;
  cursor: pointer;
  font-size: 0.9rem;
}

.ws-social:hover {
  border-color: #e5e7eb;
  color: #e5e7eb;
}

@media (max-width: 960px) {
  .ws-header {
    padding-inline: 1.5rem;
  }

  .ws-main {
    padding-inline: 1.5rem;
  }

  .ws-hero,
  .ws-features {
    grid-template-columns: minmax(0, 1fr);
  }

  .ws-hero__visual {
    order: 1;
    padding-top: 2.5rem;
  }

  .ws-hero__content {
    order: 2;
  }

  .ws-features__phone {
    margin-top: 2rem;
  }

  .ws-footer {
    flex-direction: column;
    gap: 0.75rem;
    text-align: center;
  }
}

@media (max-width: 640px) {
  .ws-header__nav {
    display: none;
  }

  .ws-header {
    padding-inline: 1.25rem;
  }

  .ws-main {
    padding-inline: 1.25rem;
  }

  .ws-hero__visual {
    padding-inline: 1rem;
  }

  .ws-hero__stores {
    flex-direction: column;
  }
}
</style>
