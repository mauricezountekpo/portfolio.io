<script setup>
import { useScrollAnimation } from './composables/useScrollAnimation'
import HeroSection from './components/HeroSection.vue'
import ContactLinks from './components/ContactLinks.vue'
import SkillsDisplay from './components/SkillsDisplay.vue'

useScrollAnimation()
</script>

<template>
  <main class="portfolio-main">
    <HeroSection>
      <template #links>
        <ContactLinks />
      </template>
    </HeroSection>

    <SkillsDisplay />
  </main>
</template>
