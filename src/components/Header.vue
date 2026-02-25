<script setup lang="ts">
import { useRouter } from 'vue-router'

const router = useRouter()

const isActive = (path: string) => {
  return router.currentRoute.value.path === path
}

const routes = [
  { path: '/', name: 'home', displayName: '首頁' },
  { path: '/privacy', name: 'privacy', displayName: '隱私政策' },
  { path: '/terms', name: 'terms', displayName: '服務條款' },
]

</script>

<template>
  <header class="ws-header">
    <div class="ws-header__logo">
      <img src="../assets/icon.png" alt="流浪靈魂" class="ws-header__logo-image">
      <span class="ws-header__logo-text">流浪靈魂</span>
    </div>
    <nav class="ws-header__nav">
      <RouterLink
        v-for="route in routes"
        :key="route.path"
        :to="route.path"
        :class="{ 'is-active': isActive(route.path) }"
      >
        {{ route.displayName }}
      </RouterLink>
    </nav>
    <button class="ws-header__cta" type="button">
      立即下載
    </button>
  </header>
</template>

<style scoped>
.ws-header {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 1.5rem 3.5rem;
  position: sticky;
  top: 0;
  z-index: 20;
  backdrop-filter: blur(16px);
  background: linear-gradient(to bottom, rgba(0, 0, 0, 0.85), transparent);
}

.ws-header__logo-image {
  width: 40px;
}

.ws-header__logo {
  display: inline-flex;
  align-items: center;
  gap: 0.6rem;
  font-weight: 600;
  letter-spacing: 0.08em;
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
  display: flex;
  gap: 1.75rem;
  font-size: 0.9rem;
}

.ws-header__nav a {
  color: #9ca3af;
  text-decoration: none;
  position: relative;
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
  padding: 0.55rem 1.4rem;
  border-radius: 999px;
  border: none;
  font-size: 0.9rem;
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
</style>