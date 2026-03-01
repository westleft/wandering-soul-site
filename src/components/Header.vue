<script setup lang="ts">
import { ref } from 'vue'
import { useRouter } from 'vue-router'

const router = useRouter()
const isMenuOpen = ref(false)

const isActive = (path: string) => {
  return router.currentRoute.value.path === path
}

const routes = [
  { path: '/', name: 'home', displayName: '首頁' },
  { path: '/privacy', name: 'privacy', displayName: '隱私政策' },
  { path: '/terms', name: 'terms', displayName: '服務條款' },
]

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}
</script>

<template>
  <header class="ws-header">
    <div class="ws-header__left">
      <div class="ws-header__logo">
        <img src="../assets/icon.png" alt="流浪靈魂" class="ws-header__logo-image">
        <span class="ws-header__logo-text">流浪靈魂</span>
      </div>
    </div>

    <nav
      class="ws-header__nav"
      :class="{ 'is-open': isMenuOpen }"
    >
      <RouterLink
        v-for="route in routes"
        :key="route.path"
        :to="route.path"
        :class="{ 'is-active': isActive(route.path) }"
        @click="isMenuOpen = false"
      >
        {{ route.displayName }}
      </RouterLink>
    </nav>

    <div class="ws-header__right">

      <button
        class="ws-header__menu-toggle"
        type="button"
        aria-label="切換主選單"
        :aria-expanded="isMenuOpen ? 'true' : 'false'"
        @click="toggleMenu"
      >
        <span class="ws-header__menu-bar" />
        <span class="ws-header__menu-bar" />
      </button>
    </div>
  </header>
</template>

<style scoped>
.ws-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1rem 1.25rem;
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(16px);
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.85), transparent);
}

.ws-header__left {
  display: flex;
  align-items: center;
  flex: 1;
}

.ws-header__right {
  display: flex;
  align-items: center;
  gap: 0.75rem;
}

.ws-header__logo-image {
  width: 32px;
}

.ws-header__logo {
  display: inline-flex;
  align-items: center;
  gap: 0.5rem;
  font-weight: 600;
  letter-spacing: 0.08em;
}

.ws-header__logo-text {
  font-size: 0.9rem;
}

.ws-header__logo-mark {
  width: 1.75rem;
  height: 1.75rem;
  border-radius: 999px;
  background: radial-gradient(circle at 30% 20%, #e5e7eb, #a855f7 40%, #1e293b 90%);
  box-shadow:
    0 0 18px rgba(168, 85, 247, 0.85),
    0 0 40px rgba(59, 130, 246, 0.85);
}

.ws-header__nav {
  position: fixed;
  inset-inline: 1.25rem;
  top: 3.5rem;
  display: none;
  flex-direction: column;
  gap: 0.75rem;
  padding: 0.75rem 0.9rem;
  border-radius: 0.9rem;
  background: rgba(15, 23, 42, 0.98);
  box-shadow:
    0 18px 45px rgba(15, 23, 42, 0.95),
    0 0 0 1px rgba(148, 163, 184, 0.4);
}

.ws-header__nav.is-open {
  display: flex;
}

.ws-header__nav a {
  color: #9ca3af;
  text-decoration: none;
  position: relative;
  padding-block: 0.25rem;
  transition:
    color 150ms ease-out,
    opacity 150ms ease-out;
}

.ws-header__nav a::after {
  content: '';
  position: absolute;
  left: 0;
  bottom: -0.3rem;
  width: 0;
  height: 2px;
  border-radius: 999px;
  background: linear-gradient(to right, #a855f7, #22d3ee);
  transition: width 160ms ease-out;
}

.ws-header__nav a:hover {
  color: #e5e7eb;
}

.ws-header__nav a:hover::after,
.ws-header__nav a.is-active::after {
  width: 100%;
}

.ws-header__cta {
  padding: 0.5rem 1.35rem;
  border-radius: 999px;
  border: none;
  font-size: 0.85rem;
  font-weight: 500;
  color: #020617;
  background: #f9fafb;
  cursor: pointer;
  box-shadow:
    0 10px 25px rgba(15, 23, 42, 0.8),
    0 0 0 1px rgba(148, 163, 184, 0.4);
  transition:
    transform 120ms ease-out,
    box-shadow 120ms ease-out,
    background 120ms ease-out;
}

.ws-header__cta:hover {
  transform: translateY(-1px);
  background: #ffffff;
  box-shadow:
    0 16px 40px rgba(15, 23, 42, 0.95),
    0 0 0 1px rgba(248, 250, 252, 0.9);
}

.ws-header__cta--mobile {
  width: 100%;
  margin-top: 0.25rem;
}

.ws-header__cta--desktop {
  display: none;
}

.ws-header__menu-toggle {
  display: flex;
  align-items: center;
  flex-direction: column;
  justify-content: center;
  gap: 0.22rem;
  width: 2.25rem;
  height: 2.25rem;
  border-radius: 999px;
  border: 1px solid rgba(148, 163, 184, 0.6);
  background: rgba(15, 23, 42, 0.95);
  cursor: pointer;
  padding: 0;
}

.ws-header__menu-bar {
  display: block;
  width: 1.1rem;
  height: 2px;
  border-radius: 999px;
  background: linear-gradient(to right, #a855f7, #22d3ee);
}

@media (min-width: 768px) {
  .ws-header {
    padding: 1.5rem 3.5rem;
  }

  .ws-header__logo-image {
    width: 40px;
  }

  .ws-header__logo-text {
    font-size: 1rem;
  }

  .ws-header__nav {
    position: static;
    inset: auto;
    top: auto;
    display: flex !important;
    flex-direction: row;
    align-items: center;
    gap: 1.75rem;
    padding: 0;
    background: transparent;
    box-shadow: none;
  }

  .ws-header__nav.is-open {
    display: flex;
  }

  .ws-header__cta--mobile {
    display: none;
  }

  .ws-header__cta--desktop {
    display: inline-flex;
  }

  .ws-header__menu-toggle {
    display: none;
  }
}
</style>