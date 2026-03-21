<script setup lang="ts">
import SoulGlow from '../SoulGlow.vue'
</script>

<template>
  <section class="hero">
    <div class="visual">
      <SoulGlow :size="240" />
      <!-- <SoulGlow2 :size="240" /> -->
    </div>
    <div class="content">
      <h1 class="title">流浪靈魂</h1>
      <p class="tagline">以缺點為主題的交友軟體</p>
      <div class="stores">
        <button class="store disabled" type="button" disabled>
          <img src="../../assets/app-store.png" alt="App Store" class="store-icon">
          <span class="store-text">
            <span class="store-label">尚未開放</span>
            <span class="store-brand">App Store</span>
          </span>
        </button>
        <button class="store disabled" type="button" disabled>
          <img src="../../assets/google-play.png" alt="Google Play" class="store-icon">
          <span class="store-text">
            <span class="store-label">尚未開放</span>
            <span class="store-brand">Google Play</span>
          </span>
        </button>
      </div>
    </div>
  </section>
</template>

<style>
@scope (.hero) {
  :scope {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 92vh;
    padding-top: 1.5rem;
  }

  .content {
    display: flex;
    flex-direction: column;
    gap: 1.75rem;
    align-items: center;
  }

  .visual {
    width: min(320px, 78vw);
    aspect-ratio: 1 / 1;
    display: grid;
    place-items: center;
  }

  .title {
    font-size: clamp(3rem, 4.2vw, 3.6rem);
    letter-spacing: 0.16em;
    font-weight: 700;
    text-align: center;
  }

  .tagline {
    font-size: 1rem;
    color: #9ca3af;
    text-align: center;
  }

  .stores {
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

  .disabled {
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

  .store-icon {
    width: 32px;
  }

  .store-text {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    line-height: 1.1;
  }

  .store-label {
    font-size: 0.6rem;
    text-transform: uppercase;
    color: #9ca3af;
    padding-bottom: 4px;
  }

  .store-brand {
    font-size: 0.95rem;
    font-weight: 600;
  }
}

@media (max-width: 640px) {
  @scope (.hero) {
    :scope {
      min-height: auto;
      padding-top: 1rem;
      gap: 2.4rem;
    }

    .visual {
      width: min(260px, 74vw);
    }

    .stores {
      flex-direction: column;
      align-items: center;
    }
  }
}
</style>
