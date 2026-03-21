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

// const glowPalette = [
//   '#5b63f0',
//   '#7b6cf6',
//   '#9a6af7',
//   '#c06bf2',
//   '#d44fa7',
//   '#e0519a',
//   '#cb4ac6',
//   '#9d46d8',
//   '#1fbf8f',
//   '#17b8a8',
//   '#1aa4c8',
//   '#3b8fe0',
//   '#d95b6a',
//   '#db6f58',
//   '#d88646',
//   '#d49a3f',
// ]

// Ocean Deep
// const glowPalette = [
//   '#1c4fd1',
//   '#2563eb',
//   '#2f7bf2',
//   '#46a0ff',
//   '#0f5f93',
//   '#1476ab',
//   '#1a8fc0',
//   '#24a8d8',
//   '#0f7c7a',
//   '#14908f',
//   '#1aa7a5',
//   '#29c2bf',
//   '#2458a8',
//   '#2d6abb',
//   '#3b81cc',
//   '#4f97dc',
// ]

// Ember Night
const glowPalette = [
  '#7a2e2e',
  '#94403a',
  '#b35345',
  '#d16951',
  '#8f3c1e',
  '#ad4a24',
  '#c85c2d',
  '#e1753b',
  '#70412d',
  '#8a4f34',
  '#a4633f',
  '#bd7851',
  '#8a2b52',
  '#a03661',
  '#b94974',
  '#cc648a',
]

// Aurora Candy
// const glowPalette = [
//   '#7b44cf',
//   '#9754da',
//   '#b668e3',
//   '#d27eea',
//   '#b13f8f',
//   '#cb4b9d',
//   '#e45eae',
//   '#f079bf',
//   '#2c9a9f',
//   '#35acb0',
//   '#43c2c4',
//   '#59d8d5',
//   '#5f4ec7',
//   '#7460d2',
//   '#8c76dc',
//   '#a591e8',
// ]

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
                  <stop offset="0%" :stop-color="glowPalette[0]" stop-opacity="1" />
                  <stop offset="25%" :stop-color="glowPalette[1]" stop-opacity="0.95" />
                  <stop offset="60%" :stop-color="glowPalette[2]" stop-opacity="0.4" />
                  <stop offset="100%" :stop-color="glowPalette[3]" stop-opacity="0" />
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
                  <stop offset="0%" :stop-color="glowPalette[4]" stop-opacity="1" />
                  <stop offset="30%" :stop-color="glowPalette[5]" stop-opacity="0.9" />
                  <stop offset="65%" :stop-color="glowPalette[6]" stop-opacity="0.35" />
                  <stop offset="100%" :stop-color="glowPalette[7]" stop-opacity="0" />
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
                  <stop offset="0%" :stop-color="glowPalette[8]" stop-opacity="1" />
                  <stop offset="28%" :stop-color="glowPalette[9]" stop-opacity="0.85" />
                  <stop offset="62%" :stop-color="glowPalette[10]" stop-opacity="0.3" />
                  <stop offset="100%" :stop-color="glowPalette[11]" stop-opacity="0" />
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
                  <stop offset="0%" :stop-color="glowPalette[12]" stop-opacity="0.95" />
                  <stop offset="32%" :stop-color="glowPalette[13]" stop-opacity="0.8" />
                  <stop offset="68%" :stop-color="glowPalette[14]" stop-opacity="0.3" />
                  <stop offset="100%" :stop-color="glowPalette[15]" stop-opacity="0" />
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
