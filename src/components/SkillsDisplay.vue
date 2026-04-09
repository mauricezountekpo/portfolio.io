<script setup>
const skills = [
  'HTML', 'CSS', 'GIT', 'GITHUB',
  'SEO', 'SASS', 'JAVASCRIPT', 'VUE.JS'
]
</script>

<template>
  <section class="section skills-section">
    <div class="container fade-target fade-up-enter">
      <span class="eyebrow">Les outils qui font la différence.</span>
      <h2 class="skills-title">Ma boîte à outils</h2>
      
      <div class="skills-grid">
        <div v-for="(skill, index) in skills" :key="index" class="skill-card bezel-outer" :style="`--delay: ${index * 0.05}s`">
          <div class="skill-inner bezel-inner">
            {{ skill }}
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.skills-section {
  text-align: center;
}

.eyebrow {
  display: block;
  font-size: 0.85rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  color: var(--accent-color);
  font-weight: 700;
  margin-bottom: 1rem;
}

.skills-title {
  margin-bottom: 4rem;
  color: var(--text-main);
}

.skills-grid {
  display: flex;
  flex-wrap: wrap;
  justify-content: center;
  gap: 1.5rem;
}

.skill-card {
  width: 220px;
  flex: 0 0 auto;
  transition: transform 0.5s cubic-bezier(0.32, 0.72, 0, 1);
  animation-delay: var(--delay);
}

.skill-inner {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1.25rem 2rem;
  font-weight: 600;
  letter-spacing: 0.05em;
  font-size: 0.9rem;
  background: var(--bezel-inner-bg);
  color: var(--text-main);
  transition: all 0.4s var(--ease-premium);
}

.skill-card:hover {
  transform: translateY(-5px) scale(1.02);
}

.skill-card:hover .skill-inner {
  background: var(--accent-light);
  box-shadow: inset 0 2px 4px rgba(15, 23, 42, 0.05);
  color: var(--accent-color);
}

@media (max-width: 768px) {
  .skills-grid {
    flex-direction: column;
    align-items: center;
  }
  .skill-card {
    width: 60%;
    min-width: 200px;
  }
}
</style>
