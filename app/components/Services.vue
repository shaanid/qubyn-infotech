<script setup>
import { Bot } from "lucide-vue-next";
</script>

<template>
  <section class="services-root" id="services">
    <div class="main-container">
      <!-- TOP FEATURED SECTION -->
      <div class="featured-service">
        <div class="featured-glow"></div>
        <div class="featured-grid">
          <div class="featured-content">
            <h2 class="featured-title">
              Engineering with precision.
              <span class="dim"
                >Build scalable systems that define the future.</span
              >
            </h2>
            <p class="featured-desc">
              Experience a new standard of productivity. We build robust,
              high-performance applications designed for security and massive
              scale.
            </p>
            <a href="#" class="featured-link">
              Explore our tech stack <span class="arrow">›</span>
            </a>
          </div>

          <div class="featured-visual">
            <div class="glass-container">
              <div class="glass-border"></div>
              <div class="card-header">
                <div class="bot-info">
                  <div class="avatar-web">
                    <Bot :size="16" stroke-width="2.5" />
                  </div>
                  <span class="bot-name">qubyn-core-engine</span>
                  <span class="bot-tag">bot</span>
                </div>
              </div>
              <div class="card-body">
                <p class="card-text">
                  Optimization complete. Improved query performance by 40% using
                  intelligent vertical scaling and caching strategies.
                </p>
                <div class="code-snippet">
                  <div class="snippet-header">
                    <span>Performance Optimization</span>
                    <span class="ai-tag">AI</span>
                  </div>
                  <div class="lines">
                    <div class="line rm">
                      <span class="ln">22</span><span class="sign">-</span>
                      <span>const data = await heavyQuery();</span>
                    </div>
                    <div class="line add">
                      <span class="ln">22</span><span class="sign">+</span>
                      <span>const data = await getCachedResults();</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <!-- BOTTOM SERVICES GRID -->
      <div class="services-bottom-grid">
        <div class="grid-item">
          <h3 class="grid-title">
            Web. <span class="light">Scalable ecosystems.</span>
          </h3>
          <p class="grid-desc">
            Reliable, secure, and modern web platforms built for high-traffic
            environments and complex workflows.
          </p>
          <a href="#" class="grid-link"
            >Explore web solutions <span class="arrow">›</span></a
          >
        </div>

        <div class="grid-item">
          <h3 class="grid-title">
            Cloud. <span class="light">Automated infra.</span>
          </h3>
          <p class="grid-desc">
            Resilient cloud architectures that scale automatically, ensuring
            maximum uptime and efficiency.
          </p>
          <a href="#" class="grid-link"
            >Learn about DevOps <span class="arrow">›</span></a
          >
        </div>

        <div class="grid-item">
          <h3 class="grid-title">
            Mobile. <span class="light">Native experiences.</span>
          </h3>
          <p class="grid-desc">
            User-centric mobile apps with flawless performance and seamless
            cross-platform synchronization.
          </p>
          <a href="#" class="grid-link"
            >View mobile portfolio <span class="arrow">›</span></a
          >
        </div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.services-root {
  background: #010409;
  color: #fff;
  padding: 120px 0;
  overflow: hidden;
}

.main-container {
  max-width: 1300px;
  margin: 0 auto;
  padding: 0 30px;
}

/* FEATURED SECTION */
.featured-service {
  position: relative;
  background: rgba(255, 255, 255, 0.01);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 40px;
  padding: 80px 60px;
  margin-bottom: 80px;
}

.featured-glow {
  position: absolute;
  top: 0;
  right: 15%;
  width: 500px;
  height: 500px;
  background: radial-gradient(
    circle,
    rgba(147, 51, 234, 0.25) 0%,
    transparent 70%
  );
  filter: blur(60px);
  z-index: 0;
  pointer-events: none;
}

.featured-grid {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 60px;
  align-items: center;
  position: relative;
  z-index: 1;
}

.featured-title {
  font-size: 2.25rem;
  font-weight: 600;
  line-height: 1.1;
  margin-bottom: 24px;
}

.featured-title .dim {
  color: #7d8590;
}

.featured-desc {
  font-size: 1.15rem;
  color: #8b949e;
  line-height: 1.6;
  margin-bottom: 32px;
  max-width: 480px;
}

.featured-link {
  color: #4493f8;
  font-weight: 600;
  text-decoration: none;
  font-size: 1.1rem;
  display: inline-flex;
  align-items: center;
  gap: 6px;
  transition: 0.2s;
}

.featured-link:hover {
  color: #58a6ff;
  transform: translateX(5px);
}

/* GLASS CARD */
.glass-container {
  position: relative;
  background: rgba(22, 27, 34, 0.8);
  backdrop-filter: blur(20px);
  border-radius: 20px;
  overflow: hidden;
  box-shadow: 0 20px 60px rgba(0, 0, 0, 0.4);
}

.glass-border {
  position: absolute;
  top: 0;
  left: 0;
  right: 0;
  bottom: 0;
  border-radius: 20px;
  padding: 1px;
  background: linear-gradient(
    135deg,
    rgba(255, 255, 255, 0.1) 0%,
    transparent 50%,
    rgba(255, 255, 255, 0.05) 100%
  );
  -webkit-mask:
    linear-gradient(#fff 0 0) content-box,
    linear-gradient(#fff 0 0);
  mask-composite: exclude;
}

.card-header {
  padding: 20px 24px;
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
}

.bot-info {
  display: flex;
  align-items: center;
  gap: 12px;
}

.avatar-web {
  width: 28px;
  height: 28px;
  background: rgba(168, 85, 247, 0.15);
  color: #bc8cff;
  border: 1px solid rgba(168, 85, 247, 0.3);
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bot-name {
  color: #c9d1d9;
  font-weight: 600;
  font-size: 14px;
}

.bot-tag {
  background: rgba(110, 118, 129, 0.1);
  border: 1px solid rgba(110, 118, 129, 0.2);
  color: #7d8590;
  font-size: 10px;
  padding: 2px 8px;
  border-radius: 12px;
  text-transform: uppercase;
}

.card-body {
  padding: 24px;
}

.card-text {
  color: #8b949e;
  font-size: 14px;
  line-height: 1.6;
  margin-bottom: 24px;
}

.code-snippet {
  background: #0d1117;
  border: 1px solid rgba(255, 255, 255, 0.1);
  border-radius: 12px;
  overflow: hidden;
  font-family: "JetBrains Mono", monospace;
}

.snippet-header {
  padding: 10px 16px;
  background: rgba(255, 255, 255, 0.02);
  border-bottom: 1px solid rgba(255, 255, 255, 0.05);
  display: flex;
  justify-content: space-between;
  align-items: center;
  font-size: 11px;
  color: #7d8590;
}

.ai-tag {
  background: rgba(168, 85, 247, 0.1);
  color: #bc8cff;
  border: 1px solid rgba(168, 85, 247, 0.2);
  padding: 1px 4px;
  border-radius: 4px;
}

.lines {
  padding: 12px 0;
  font-size: 12px;
}

.line {
  display: flex;
  padding: 2px 16px;
  gap: 10px;
}

.line.rm {
  background: rgba(248, 81, 73, 0.08);
  color: #ff7b72;
}
.line.add {
  background: rgba(46, 160, 67, 0.1);
  color: #7ee787;
}
.ln {
  opacity: 0.3;
  width: 20px;
  text-align: right;
}
.sign {
  width: 10px;
}

/* SERVICES GRID */
.services-bottom-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.grid-item {
  display: flex;
  flex-direction: column;
}

.grid-title {
  font-size: 1.25rem;
  font-weight: 600;
  margin-bottom: 12px;
}

.grid-title .light {
  color: #7d8590;
  font-weight: 400;
}

.grid-desc {
  font-size: 1rem;
  color: #7d8590;
  line-height: 1.5;
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
  transition: 0.2s;
}

.grid-link:hover {
  color: #58a6ff;
  transform: translateX(3px);
}

/* RESPONSIVE */
@media (max-width: 1100px) {
  .featured-grid {
    grid-template-columns: 1fr;
    text-align: center;
  }
  .featured-content {
    max-width: 100%;
  }
  .featured-desc {
    margin-left: auto;
    margin-right: auto;
  }
  .featured-link {
    justify-content: center;
  }
  .services-bottom-grid {
    grid-template-columns: 1fr 1fr;
  }
}

@media (max-width: 768px) {
  .featured-service {
    padding: 40px 30px;
    border-radius: 30px;
  }
  .featured-title {
    font-size: 1.75rem;
  }
  .services-bottom-grid {
    grid-template-columns: 1fr;
    gap: 50px;
  }
  .main-container {
    padding: 0 20px;
  }
}
</style>
