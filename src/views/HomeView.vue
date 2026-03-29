<script setup lang="ts">
import FeaturesSection from '../components/home/FeaturesSection.vue'
import FaqSection from '../components/home/FaqSection.vue'
import HeroSection from '../components/home/HeroSection.vue'
import MarqueeSection from '../components/home/MarqueeSection.vue'
import StorySection from '../components/home/StorySection.vue'
</script>

<template>
  <div class="ws">
    <main class="main" id="top">
      <HeroSection />
      <StorySection />
      <FeaturesSection />
      <MarqueeSection />
      <FaqSection />
    </main>
  </div>
</template>

<style>
@scope (.ws) {
  :scope {
    min-height: 100vh;
    display: flex;
    flex-direction: column;
    color: #e5e7eb;
    background-color: #192955;
  }

  .main {
    flex: 1;
    display: flex;
    flex-direction: column;
    gap: 1.2rem;
  }
}

@media (max-width: 960px) {
  @scope (.ws) {
    .main {
      padding-inline: 1.5rem;
    }
  }
}

@media (max-width: 640px) {
  @scope (.ws) {
    .main {
      padding-inline: 1.25rem;
    }
  }
}
</style>
