<template>
  <div class="links-stack fade-target fade-up-enter">
    <a href="mailto:mauricezountekpo@proton.me" class="mag-btn secondary group">
      <span class="btn-text">Contact</span>
      <span class="btn-icon-wrapper" aria-hidden="true">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" class="icon"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"></path></svg>
      </span>
    </a>

    <a href="https://github.com/mauricezountekpo" target="_blank" rel="noopener noreferrer" class="mag-btn group">
      <span class="btn-text">Github</span>
      <span class="btn-icon-wrapper" aria-hidden="true">
        <svg fill="none" stroke="currentColor" viewBox="0 0 24 24" class="icon"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="1.5" d="M14 5l7 7m0 0l-7 7m7-7H3"></path></svg>
      </span>
    </a>
  </div>
</template>

<style scoped>
.links-stack {
  display: flex;
  gap: 1.25rem;
  margin-top: 3rem;
  flex-wrap: wrap;
}

.mag-btn {
  display: inline-flex;
  align-items: center;
  background: var(--text-main);
  color: var(--bg-color);
  padding: 0.5rem 0.65rem 0.5rem 1.75rem;
  border-radius: 9999px;
  font-weight: 600;
  cursor: pointer;
  transition: transform 0.4s var(--ease-premium), background-color 0.4s ease;
  position: relative;
  overflow: hidden;
  text-decoration: none;
}

.secondary {
  background: transparent;
  color: var(--text-main);
  border: 1px solid rgba(15, 23, 42, 0.15);
}

.mag-btn:active {
  transform: scale(0.98);
}

.btn-text {
  margin-right: 1.5rem;
  font-size: 0.95rem;
  letter-spacing: -0.01em;
}

/* Architecture Button-in-Button */
.btn-icon-wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 2.75rem;
  height: 2.75rem;
  background: rgba(255, 255, 255, 0.15);
  border-radius: 50%;
  color: inherit;
  transition: transform 0.4s var(--ease-premium);
}

.secondary .btn-icon-wrapper {
  background: rgba(15, 23, 42, 0.05);
}

.icon {
  width: 1.2rem;
  height: 1.2rem;
  transition: transform 0.4s var(--ease-premium);
}

/* Physique Magnétique au Hover */
.mag-btn.group:hover .btn-icon-wrapper {
  transform: scale(1.05) translate(2px, -1px);
}

.mag-btn.group:hover .icon {
  transform: translate(1px, -1px);
}

.secondary.group:hover {
  background: rgba(15, 23, 42, 0.03);
  border-color: rgba(15, 23, 42, 0.25);
}
</style>
