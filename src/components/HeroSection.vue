<template>
  <section class="section hero-section">
    <div class="container hero-layout">
      <!-- Left: Typography -->
      <div class="text-content fade-target fade-up-enter">
        <span class="eyebrow">Développeur Front-End</span>
        <h1>ZOUNTEKPO<br/><span class="text-gradient">Maurice</span></h1>
        <p class="subtitle">Votre prochain projet mérite un développeur qui pense autant à l'utilisateur qu'à la ligne de code ;</p>

        <slot name="links"></slot>
      </div>

      <!-- Right: Image with Animated Ring -->
      <div class="image-wrapper fade-target fade-up-enter">
        <div class="avatar-container">
          <div class="avatar-ring" aria-hidden="true"></div>
          <img src="/maurice_zountekpo.png" alt="maurice_zountekpo_photo" class="profile-img" />
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.hero-section {
  display: flex;
  align-items: center;
  min-height: 100vh;
}

.hero-layout {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
}

@media (max-width: 992px) {
  .hero-layout {
    grid-template-columns: 1fr;
    text-align: left;
    padding-top: 4rem;
  }
}

.eyebrow {
  display: inline-block;
  font-size: 0.9rem;
  font-weight: 600;
  letter-spacing: 0.1em;
  text-transform: uppercase;
  color: var(--accent-color);
  margin-bottom: 1.5rem;
}

.text-gradient {
  background: linear-gradient(135deg, var(--accent-color) 0%, #3B82F6 100%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
}

.subtitle {
  font-size: 1.25rem;
  line-height: 1.6;
  color: var(--text-muted);
  margin-top: 1.5rem;
  margin-bottom: 2rem;
  max-width: 480px;
}

/* Animated Circular Image Setup */
.image-wrapper {
  display: flex;
  justify-content: center;
  align-items: center;
}

.avatar-container {
  position: relative;
  width: clamp(280px, 35vw, 420px);
  aspect-ratio: 1;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* The spinning gradient ring */
.avatar-ring {
  position: absolute;
  inset: -12px;
  border-radius: 50%;
  background: conic-gradient(
    from 0deg,
    transparent 0%,
    transparent 40%,
    var(--accent-color) 80%,
    transparent 100%
  );
  animation: spin-ring 5s linear infinite;
  opacity: 0.8;
  transition: opacity 0.4s ease, filter 0.4s ease;
}

/* Internal cutout to make the gradient look like a border */
.avatar-ring::before {
  content: "";
  position: absolute;
  inset: 2px;
  background: var(--bg-color);
  border-radius: 50%;
}

@keyframes spin-ring {
  100% {
    transform: rotate(360deg);
  }
}

.profile-img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  border-radius: 50%;
  position: relative;
  z-index: 2;
  border: 6px solid var(--bg-color);
  box-shadow: 0 10px 30px -5px rgba(15, 23, 42, 0.15);
  background: var(--bezel-inner-bg);
  transition: transform 0.6s var(--ease-premium);
}

.avatar-container:hover .profile-img {
  transform: scale(1.03);
}

.avatar-container:hover .avatar-ring {
  opacity: 1;
  filter: drop-shadow(0 0 10px rgba(30, 58, 138, 0.4));
}
</style>
