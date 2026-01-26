<template>
  <section class="trusted-root">
    <!-- Ambient Glows -->
    <div class="ambient-glow"></div>

    <div class="main-container">
      <div class="header-container">
        <h2 class="section-tag">Trusted by innovative teams</h2>
      </div>

      <div class="ticker-wrapper">
        <div class="ticker-content">
          <div v-for="(logo, index) in logos" :key="index" class="logo-chip">
            <span class="logo-text">{{ logo }}</span>
            <div class="chip-glow"></div>
          </div>
          <!-- Duplicate for seamless scroll -->
          <div
            v-for="(logo, index) in logos"
            :key="'dup-' + index"
            class="logo-chip"
          >
            <span class="logo-text">{{ logo }}</span>
            <div class="chip-glow"></div>
          </div>
        </div>
      </div>

      <div class="bottom-gradient"></div>
    </div>
  </section>
</template>

<script setup>
const logos = [
  "Stripe",
  "Nvidia",
  "OpenAI",
  "Google",
  "Microsoft",
  "AWS",
  "Vercel",
  "GitHub",
];
</script>

<style scoped>
.trusted-root {
  position: relative;
  background: #020408;
  padding: 100px 0;
  overflow: hidden;
  border-top: 1px solid rgba(255, 255, 255, 0.03);
  border-bottom: 1px solid rgba(255, 255, 255, 0.03);
}

.ambient-glow {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  width: 1000px;
  height: 400px;
  background: radial-gradient(
    circle at center,
    rgba(139, 92, 246, 0.03) 0%,
    transparent 70%
  );
  z-index: 0;
  pointer-events: none;
}

.main-container {
  max-width: 1216px;
  margin: 0 auto;
  padding: 0 32px;
  position: relative;
  z-index: 1;
}

.header-container {
  text-align: center;
  margin-bottom: 60px;
}

.section-tag {
  color: #8b949e;
  font-size: 0.75rem;
  font-weight: 600;
  text-transform: uppercase;
  letter-spacing: 0.25em;
  opacity: 0.8;
}

/* Logo Ticker Styling */
.ticker-wrapper {
  mask-image: linear-gradient(
    to right,
    transparent,
    black 15%,
    black 85%,
    transparent
  );
  -webkit-mask-image: linear-gradient(
    to right,
    transparent,
    black 15%,
    black 85%,
    transparent
  );
  width: 100%;
  overflow: hidden;
}

.ticker-content {
  display: flex;
  gap: 48px;
  width: max-content;
  animation: scroll 40s linear infinite;
  padding: 12px 0;
}

.logo-chip {
  position: relative;
  background: rgba(255, 255, 255, 0.02);
  border: 1px solid rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(8px);
  padding: 20px 48px;
  border-radius: 100px;
  transition: all 0.4s cubic-bezier(0.4, 0, 0.2, 1);
  display: flex;
  align-items: center;
  justify-content: center;
  cursor: pointer;
}

.logo-text {
  color: #c9d1d9;
  font-size: 1.125rem;
  font-weight: 500;
  letter-spacing: -0.01em;
  transition: color 0.3s ease;
  z-index: 2;
}

.logo-chip:hover {
  background: rgba(255, 255, 255, 0.05);
  border-bordercolor: rgba(255, 255, 255, 0.15);
  transform: translateY(-2px);
}

.logo-chip:hover .logo-text {
  color: #ffffff;
}

/* Internal glow on hover */
.chip-glow {
  position: absolute;
  inset: 0;
  border-radius: 100px;
  background: radial-gradient(
    circle at center,
    rgba(188, 140, 255, 0.1) 0%,
    transparent 70%
  );
  opacity: 0;
  transition: opacity 0.4s ease;
  z-index: 1;
}

.logo-chip:hover .chip-glow {
  opacity: 1;
}

@keyframes scroll {
  0% {
    transform: translateX(0);
  }
  100% {
    transform: translateX(calc(-50% - 24px));
  }
}

/* Responsive */
@media (max-width: 768px) {
  .logo-chip {
    padding: 16px 36px;
  }
  .logo-text {
    font-size: 1rem;
  }
  .section-tag {
    font-size: 0.7rem;
  }
}
</style>
