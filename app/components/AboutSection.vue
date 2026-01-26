<template>
  <section class="about-root" id="about">
    <div class="main-container">
      <!-- TOP FEATURED SECTION (Matching Services Design) -->
      <div class="featured-about" ref="aboutRef">
        <!-- Re-adding the realistic glass reflection from services style -->
        <div class="glass-sheen"></div>
        <div class="featured-glow"></div>

        <div class="featured-grid">
          <div class="featured-content">
            <h2 class="featured-title">
              Driven by engineering
              <span class="dim">excellence and innovation.</span>
            </h2>
            <p class="featured-desc">
              At Qubyn Infotech, we believe technology is the catalyst for
              growth. We build robust, scalable, and forward-thinking software
              solutions.
            </p>
            <a href="#" class="featured-link">
              Read our story <span class="arrow">›</span>
            </a>
          </div>

          <div class="featured-visual">
            <div class="stats-card">
              <div v-for="(stat, index) in stats" :key="index" class="stat-box">
                <div class="stat-value">
                  {{ Math.floor(displayStats[index]) }}{{ stat.suffix }}
                </div>
                <div class="stat-label">{{ stat.label }}</div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="full-width-line"></div>

      <!-- BOTTOM VALUES GRID (Matching Services Design) -->
      <div class="values-bottom-grid">
        <div v-for="(item, index) in values" :key="index" class="grid-item">
          <div class="icon-wrap" :style="{ color: item.color }">
            <component :is="item.icon" :size="24" stroke-width="2.5" />
          </div>
          <h3 class="grid-title">
            {{ item.title }}. <span class="light">{{ item.subtitle }}</span>
          </h3>
          <p class="grid-desc">{{ item.desc }}</p>
          <a href="#" class="grid-link"
            >Learn more <span class="arrow">›</span></a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref, onMounted } from "vue";
import { Target, Eye, Users } from "lucide-vue-next";

const values = [
  {
    title: "Mission",
    subtitle: "Accelerate growth.",
    desc: "To accelerate digital transformation for enterprises through cutting-edge technology and engineering.",
    icon: Target,
    color: "#bc8cff",
  },
  {
    title: "Vision",
    subtitle: "Seamless software.",
    desc: "A world where software is seamless, secure, and intuitive—bridging the gap between human potential.",
    icon: Eye,
    color: "#4493f8",
  },
  {
    title: "Team",
    subtitle: "Passionate experts.",
    desc: "A collective of passionate engineers, designers, and strategists dedicated to crafting user experiences.",
    icon: Users,
    color: "#ff7bbd",
  },
];

const stats = [
  { value: 5, suffix: "+", label: "Years Experience" },
  { value: 50, suffix: "+", label: "Projects Delivered" },
  { value: 100, suffix: "%", label: "Satisfaction Rate" },
];

const displayStats = ref(stats.map(() => 0));
const aboutRef = ref(null);
const hasAnimated = ref(false);

const animateStats = () => {
  if (hasAnimated.value) return;
  hasAnimated.value = true;

  stats.forEach((stat, index) => {
    const duration = 2000;
    const startTime = performance.now();

    const update = (currentTime) => {
      const elapsed = currentTime - startTime;
      const progress = Math.min(elapsed / duration, 1);

      // Easing function (easeOutExpo)
      const easeProgress = progress === 1 ? 1 : 1 - Math.pow(2, -10 * progress);

      displayStats.value[index] = easeProgress * stat.value;

      if (progress < 1) {
        requestAnimationFrame(update);
      }
    };

    requestAnimationFrame(update);
  });
};

onMounted(() => {
  const observer = new IntersectionObserver(
    (entries) => {
      if (entries[0].isIntersecting) {
        animateStats();
        observer.disconnect();
      }
    },
    { threshold: 0.2 },
  );

  if (aboutRef.value) {
    observer.observe(aboutRef.value);
  }
});
</script>

<style scoped>
.about-root {
  background: #020408;
  color: #fff;
  padding: 120px 0;
  overflow: hidden;
  position: relative;
}

.main-container {
  max-width: 1216px;
  margin: 0 auto;
  padding: 0 32px;
}

/* FEATURED SECTION (MATCHING SERVICES) */
.featured-about {
  position: relative;
  background:
    linear-gradient(#020408, #020408) padding-box,
    linear-gradient(
        135deg,
        rgba(255, 255, 255, 0.2) 0%,
        rgba(255, 255, 255, 0.05) 50%,
        rgba(255, 255, 255, 0.1) 100%
      )
      border-box;
  border: 1px solid transparent;
  border-bottom: none;
  border-radius: 24px 24px 0 0;
  padding: 80px 60px;
  overflow: hidden;
}

.glass-sheen {
  position: absolute;
  top: 0;
  left: 0;
  width: 200px;
  height: 200px;
  background: radial-gradient(
    circle at 0% 0%,
    rgba(255, 255, 255, 0.15) 0%,
    transparent 70%
  );
  z-index: 2;
  pointer-events: none;
}

.featured-glow {
  position: absolute;
  top: -200px;
  left: 50%;
  transform: translateX(-50%);
  width: 800px;
  height: 600px;
  background: radial-gradient(
    circle,
    rgba(139, 92, 246, 0.1) 0%,
    transparent 70%
  );
  filter: blur(80px);
  z-index: 0;
}

.featured-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 80px;
  align-items: center;
  position: relative;
  z-index: 1;
}

.featured-title {
  font-size: 2.5rem;
  font-weight: 700;
  line-height: 1.2;
  margin-bottom: 24px;
  letter-spacing: -0.02em;
}

.featured-title .dim {
  color: #8b949e;
  display: block;
}

.featured-desc {
  font-size: 1.25rem;
  color: #8b949e;
  line-height: 1.5;
  margin-bottom: 32px;
  max-width: 440px;
}

.featured-link {
  color: #4493f8;
  font-weight: 600;
  text-decoration: none;
  font-size: 1rem;
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

/* STATS CARD DESIGN */
.stats-card {
  background: rgba(255, 255, 255, 0.03);
  backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;
  padding: 40px;
  display: flex;
  flex-direction: column;
  gap: 32px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
}

.stat-box {
  display: flex;
  flex-direction: column;
}

.stat-value {
  font-size: 3rem;
  font-weight: 800;
  color: #fff;
  line-height: 1;
  margin-bottom: 4px;
  letter-spacing: -0.02em;
}

.stat-label {
  color: #8b949e;
  font-size: 0.9rem;
  text-transform: uppercase;
  letter-spacing: 0.1em;
}

.full-width-line {
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
  width: 100vw;
  margin-left: calc(-50vw + 50%);
}

/* BOTTOM VALUES GRID */
.values-bottom-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  background:
    linear-gradient(#020408, #020408) padding-box,
    linear-gradient(
        180deg,
        rgba(255, 255, 255, 0.1) 0%,
        rgba(255, 255, 255, 0.05) 100%
      )
      border-box;
  border: 1px solid transparent;
  border-top: none;
  margin-bottom: 48px;
}

.grid-item {
  display: flex;
  flex-direction: column;
  padding: 48px 40px;
}

.grid-item:not(:first-child) {
  border-left: 1px solid rgba(255, 255, 255, 0.1);
}

.icon-wrap {
  margin-bottom: 20px;
  background: rgba(255, 255, 255, 0.03);
  width: 48px;
  height: 48px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.05);
}

.grid-title {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 8px;
}

.grid-title .light {
  color: #8b949e;
  font-weight: 400;
}

.grid-desc {
  font-size: 0.95rem;
  color: #8b949e;
  line-height: 1.6;
  margin-bottom: 20px;
  flex-grow: 1;
}

.grid-link {
  color: #4493f8;
  font-weight: 600;
  text-decoration: none;
  font-size: 0.95rem;
  display: inline-flex;
  align-items: center;
  gap: 4px;
}

@media (max-width: 1024px) {
  .featured-grid {
    grid-template-columns: 1fr;
    gap: 48px;
  }
  .featured-about {
    padding: 60px 40px;
  }
  .values-bottom-grid {
    grid-template-columns: 1fr;
  }
  .grid-item {
    padding: 32px 0;
    border-left: none !important;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  .grid-item:last-child {
    border-bottom: none;
  }
}
</style>
