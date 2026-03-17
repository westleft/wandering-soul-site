<script setup lang="ts">
import { computed } from 'vue'
import type { CSSProperties } from 'vue'

let soulGlowInstance = 0

const props = withDefaults(
  defineProps<{
    size?: number
  }>(),
  {
    size: 200,
  },
)

const instanceId = ++soulGlowInstance

const gradientIds = {
  glow1: `soul-glow-${instanceId}-1`,
  glow2: `soul-glow-${instanceId}-2`,
  glow3: `soul-glow-${instanceId}-3`,
  glow4: `soul-glow-${instanceId}-4`,
}

const containerStyle = computed<CSSProperties>(() => ({
  width: `${props.size}px`,
  height: `${props.size}px`,
  '--soul-movement-factor': `${props.size / 200}`,
}))
</script>

<template>
  <div class="soul-glow" :style="containerStyle">
    <div class="soul-glow__layer">
      <div class="soul-glow__tx soul-glow__tx--1">
        <div class="soul-glow__ty soul-glow__ty--1">
          <div class="soul-glow__scale soul-glow__scale--1 soul-glow__opacity--1">
            <svg viewBox="0 0 100 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">
              <defs>
                <radialGradient :id="gradientIds.glow1" cx="50%" cy="50%" r="50%">
                  <stop offset="0%" stop-color="#818cf8" stop-opacity="1" />
                  <stop offset="25%" stop-color="#a78bfa" stop-opacity="0.95" />
                  <stop offset="60%" stop-color="#c084fc" stop-opacity="0.4" />
                  <stop offset="100%" stop-color="#e879f9" stop-opacity="0" />
                </radialGradient>
              </defs>
              <rect width="100" height="100" :fill="`url(#${gradientIds.glow1})`" />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <div class="soul-glow__layer">
      <div class="soul-glow__tx soul-glow__tx--2">
        <div class="soul-glow__ty soul-glow__ty--2">
          <div class="soul-glow__scale soul-glow__scale--2 soul-glow__opacity--2">
            <svg viewBox="0 0 100 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">
              <defs>
                <radialGradient :id="gradientIds.glow2" cx="50%" cy="50%" r="50%">
                  <stop offset="0%" stop-color="#f472b6" stop-opacity="1" />
                  <stop offset="30%" stop-color="#ec4899" stop-opacity="0.9" />
                  <stop offset="65%" stop-color="#a855f7" stop-opacity="0.35" />
                  <stop offset="100%" stop-color="#a855f7" stop-opacity="0" />
                </radialGradient>
              </defs>
              <rect width="100" height="100" :fill="`url(#${gradientIds.glow2})`" />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <div class="soul-glow__layer">
      <div class="soul-glow__tx soul-glow__tx--3">
        <div class="soul-glow__ty soul-glow__ty--3">
          <div class="soul-glow__scale soul-glow__scale--3 soul-glow__opacity--3">
            <svg viewBox="0 0 100 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">
              <defs>
                <radialGradient :id="gradientIds.glow3" cx="50%" cy="50%" r="50%">
                  <stop offset="0%" stop-color="#34d399" stop-opacity="1" />
                  <stop offset="28%" stop-color="#22d3ee" stop-opacity="0.85" />
                  <stop offset="62%" stop-color="#38bdf8" stop-opacity="0.3" />
                  <stop offset="100%" stop-color="#60a5fa" stop-opacity="0" />
                </radialGradient>
              </defs>
              <rect width="100" height="100" :fill="`url(#${gradientIds.glow3})`" />
            </svg>
          </div>
        </div>
      </div>
    </div>

    <div class="soul-glow__layer">
      <div class="soul-glow__tx soul-glow__tx--4">
        <div class="soul-glow__ty soul-glow__ty--4">
          <div class="soul-glow__scale soul-glow__scale--4 soul-glow__opacity--4">
            <svg viewBox="0 0 100 100" preserveAspectRatio="xMidYMid meet" aria-hidden="true">
              <defs>
                <radialGradient :id="gradientIds.glow4" cx="50%" cy="50%" r="50%">
                  <stop offset="0%" stop-color="#fb7185" stop-opacity="0.95" />
                  <stop offset="32%" stop-color="#f87171" stop-opacity="0.8" />
                  <stop offset="68%" stop-color="#fb923c" stop-opacity="0.3" />
                  <stop offset="100%" stop-color="#fbbf24" stop-opacity="0" />
                </radialGradient>
              </defs>
              <rect width="100" height="100" :fill="`url(#${gradientIds.glow4})`" />
            </svg>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style scoped>
.soul-glow {
  position: relative;
  display: block;
}

.soul-glow__layer {
  position: absolute;
  inset: 0;
}

.soul-glow__tx,
.soul-glow__ty,
.soul-glow__scale {
  position: absolute;
  inset: 0;
  transform-origin: center;
  will-change: transform, opacity;
}

.soul-glow__scale svg {
  width: 100%;
  height: 100%;
  display: block;
}

.soul-glow__tx--1 {
  animation: soul-x-1 10000ms ease-in-out infinite alternate;
}

.soul-glow__ty--1 {
  animation: soul-y-1 9000ms ease-in-out infinite alternate;
}

.soul-glow__scale--1 {
  animation: soul-scale-1 7000ms ease-in-out infinite alternate;
}

.soul-glow__opacity--1 {
  animation: soul-opacity-1 6000ms ease-in-out infinite alternate;
}

.soul-glow__tx--2 {
  animation: soul-x-2 8400ms ease-in-out infinite alternate;
}

.soul-glow__ty--2 {
  animation: soul-y-2 7600ms ease-in-out infinite alternate;
}

.soul-glow__scale--2 {
  animation: soul-scale-2 5600ms ease-in-out infinite alternate;
}

.soul-glow__opacity--2 {
  animation: soul-opacity-2 5000ms ease-in-out infinite alternate;
}

.soul-glow__tx--3 {
  animation: soul-x-3 7200ms ease-in-out infinite alternate;
}

.soul-glow__ty--3 {
  animation: soul-y-3 6400ms ease-in-out infinite alternate;
}

.soul-glow__scale--3 {
  animation: soul-scale-3 4400ms ease-in-out infinite alternate;
}

.soul-glow__opacity--3 {
  animation: soul-opacity-3 4000ms ease-in-out infinite alternate;
}

.soul-glow__tx--4 {
  animation: soul-x-4 9600ms ease-in-out infinite alternate;
}

.soul-glow__ty--4 {
  animation: soul-y-4 8200ms ease-in-out infinite alternate;
}

.soul-glow__scale--4 {
  animation: soul-scale-4 8000ms ease-in-out infinite alternate;
}

.soul-glow__opacity--4 {
  animation: soul-opacity-4 7000ms ease-in-out infinite alternate;
}

@keyframes soul-x-1 {
  0% { transform: translateX(0); }
  50% { transform: translateX(calc(25px * var(--soul-movement-factor))); }
  100% { transform: translateX(calc(-25px * var(--soul-movement-factor))); }
}

@keyframes soul-y-1 {
  0% { transform: translateY(0); }
  50% { transform: translateY(calc(20px * var(--soul-movement-factor))); }
  100% { transform: translateY(calc(-20px * var(--soul-movement-factor))); }
}

@keyframes soul-scale-1 {
  0% { transform: scale(1); }
  50% { transform: scale(1.3); }
  100% { transform: scale(0.9); }
}

@keyframes soul-opacity-1 {
  0% { opacity: 0.9; }
  50% { opacity: 1; }
  100% { opacity: 0.7; }
}

@keyframes soul-x-2 {
  0% { transform: translateX(0); }
  50% { transform: translateX(calc(-22px * var(--soul-movement-factor))); }
  100% { transform: translateX(calc(22px * var(--soul-movement-factor))); }
}

@keyframes soul-y-2 {
  0% { transform: translateY(0); }
  50% { transform: translateY(calc(-25px * var(--soul-movement-factor))); }
  100% { transform: translateY(calc(25px * var(--soul-movement-factor))); }
}

@keyframes soul-scale-2 {
  0% { transform: scale(1); }
  50% { transform: scale(1.25); }
  100% { transform: scale(0.92); }
}

@keyframes soul-opacity-2 {
  0% { opacity: 0.8; }
  50% { opacity: 0.95; }
  100% { opacity: 0.65; }
}

@keyframes soul-x-3 {
  0% { transform: translateX(0); }
  50% { transform: translateX(calc(20px * var(--soul-movement-factor))); }
  100% { transform: translateX(calc(-20px * var(--soul-movement-factor))); }
}

@keyframes soul-y-3 {
  0% { transform: translateY(0); }
  50% { transform: translateY(calc(22px * var(--soul-movement-factor))); }
  100% { transform: translateY(calc(-22px * var(--soul-movement-factor))); }
}

@keyframes soul-scale-3 {
  0% { transform: scale(1); }
  50% { transform: scale(1.2); }
  100% { transform: scale(0.9); }
}

@keyframes soul-opacity-3 {
  0% { opacity: 0.7; }
  50% { opacity: 0.9; }
  100% { opacity: 0.6; }
}

@keyframes soul-x-4 {
  0% { transform: translateX(0); }
  50% { transform: translateX(calc(-18px * var(--soul-movement-factor))); }
  100% { transform: translateX(calc(18px * var(--soul-movement-factor))); }
}

@keyframes soul-y-4 {
  0% { transform: translateY(0); }
  50% { transform: translateY(calc(20px * var(--soul-movement-factor))); }
  100% { transform: translateY(calc(-20px * var(--soul-movement-factor))); }
}

@keyframes soul-scale-4 {
  0% { transform: scale(1); }
  50% { transform: scale(1.15); }
  100% { transform: scale(0.95); }
}

@keyframes soul-opacity-4 {
  0% { opacity: 0.75; }
  50% { opacity: 0.85; }
  100% { opacity: 0.55; }
}
</style>
