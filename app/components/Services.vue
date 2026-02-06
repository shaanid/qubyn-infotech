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
                >Build systems that scale with your ambition.</span
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
            <div class="outer-card">
              <div class="card-header-main">
                <div class="bot-info-main">
                  <div class="avatar-circle">
                    <Bot :size="16" stroke-width="2.5" />
                  </div>
                  <span class="bot-name-main">qubyn-performance-lab</span>
                  <span class="bot-tag-main">bot</span>
                </div>
              </div>
              <div class="card-body-main">
                <p class="card-text-main">
                  Optimized the auto-scaling policy for high-concurrency
                  traffic. Switching to predictive scaling to ensure 99.99%
                  uptime during peak loads.
                </p>

                <!-- Inner Code Card -->
                <div class="inner-code-card">
                  <div class="inner-header">
                    <div class="ai-sparkle">
                      <svg
                        class="w-4 h-4"
                        fill="currentColor"
                        viewBox="0 0 24 24"
                      >
                        <path
                          d="M12 2L14.5 9L22 12L14.5 15L12 22L9.5 15L2 12L9.5 9L12 2Z"
                        />
                      </svg>
                    </div>
                    <span>Qubyn Autofix</span>
                    <span class="ai-badge">AI</span>
                  </div>
                  <div class="code-diff">
                    <div class="diff-line">
                      <span class="line-num">1</span>
                      <span class="content">const config = {</span>
                    </div>
                    <div class="diff-line rm">
                      <span class="line-num">2</span>
                      <span class="sign">-</span>
                      <span class="content"> replicas: "auto",</span>
                    </div>
                    <div class="diff-line add">
                      <span class="line-num">2</span>
                      <span class="sign">+</span>
                      <span class="content"> replicas: "predictive",</span>
                    </div>
                    <div class="diff-line add">
                      <span class="line-num">3</span>
                      <span class="sign">+</span>
                      <span class="content"> minNodes: 5</span>
                    </div>
                    <div class="diff-line">
                      <span class="line-num">4</span>
                      <span class="content">};</span>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>

      <div class="full-width-line"></div>

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
  background: #020408;
  color: #fff;
  padding: 120px 0;
  overflow: hidden;
  position: relative;
}

@media (max-width: 768px) {
  .services-root {
    padding: 64px 0;
  }
}

.main-container {
  max-width: 1216px;
  margin: 0 auto;
  padding: 0 32px;
}

/* FEATURED SECTION */
.featured-service {
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
  margin-bottom: 0;
  overflow: hidden;
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
    rgba(147, 51, 234, 0.15) 0%,
    transparent 70%
  );
  filter: blur(80px);
  z-index: 0;
  pointer-events: none;
}

.featured-grid {
  display: grid;
  grid-template-columns: 1fr 1.2fr;
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
  transition: 0.2s;
}

.featured-link:hover {
  text-decoration: underline;
}

/* CARDS DESIGN */
.outer-card {
  background: rgba(255, 255, 255, 0.03);
  backdrop-filter: blur(12px);
  -webkit-backdrop-filter: blur(12px);
  border: 1px solid rgba(255, 255, 255, 0.08);
  border-radius: 16px;
  padding: 24px;
  box-shadow: 0 8px 32px rgba(0, 0, 0, 0.4);
}

.card-header-main {
  margin-bottom: 16px;
}

.bot-info-main {
  display: flex;
  align-items: center;
  gap: 12px;
}

.avatar-circle {
  width: 28px;
  height: 28px;
  background: rgba(168, 85, 247, 0.1);
  color: #bc8cff;
  border-radius: 50%;
  display: flex;
  align-items: center;
  justify-content: center;
}

.bot-name-main {
  color: #c9d1d9;
  font-weight: 600;
  font-size: 14px;
}

.bot-tag-main {
  color: #8b949e;
  font-size: 12px;
  border: 1px solid #30363d;
  padding: 1px 6px;
  border-radius: 10px;
}

.card-text-main {
  color: #8b949e;
  font-size: 14px;
  line-height: 1.6;
  margin-bottom: 24px;
}

.inner-code-card {
  background: white;
  border-radius: 12px;
  overflow: hidden;
  color: #1f2328;
}

.inner-header {
  padding: 12px 16px;
  background: #f6f8fa;
  border-bottom: 1px solid #d0d7de;
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 13px;
  font-weight: 600;
}

.ai-sparkle {
  color: #8250df;
}

.ai-badge {
  background: #eff1f3;
  border: 1px solid #d0d7de;
  color: #656d76;
  font-size: 10px;
  padding: 1px 4px;
  border-radius: 4px;
}

.code-diff {
  padding: 12px 0;
  font-family:
    ui-monospace, SFMono-Regular, "SF Mono", Menlo, Consolas, "Liberation Mono",
    monospace;
  font-size: 12px;
}

.diff-line {
  display: flex;
  padding: 0 16px;
  gap: 8px;
  line-height: 20px;
}

.line-num {
  width: 20px;
  color: #656d76;
  text-align: right;
  user-select: none;
}

.diff-line.rm {
  background: #ffebe9;
}
.diff-line.add {
  background: #dafbe1;
}

.sign {
  width: 10px;
  font-weight: 600;
}

.diff-line.rm .sign {
  color: #cf222e;
}
.diff-line.add .sign {
  color: #1a7f37;
}

/* SERVICES GRID */
.services-bottom-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 0;
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
  border-radius: 0;
  padding: 0;
  margin-bottom: 48px;
}

.full-width-line {
  height: 1px;
  background: rgba(255, 255, 255, 0.1);
  width: 100vw;
  margin-left: calc(-50vw + 50%);
  pointer-events: none;
}

.grid-item {
  display: flex;
  flex-direction: column;
  padding: 48px 40px;
}

/* Vertical Separators using borders */
.grid-item:not(:first-child) {
  border-left: 1px solid rgba(255, 255, 255, 0.1);
}

.grid-title {
  font-size: 1.1rem;
  font-weight: 700;
  margin-bottom: 8px;
  line-height: 1.4;
}

.grid-title .light {
  color: #8b949e;
  font-weight: 400;
}

.grid-desc {
  font-size: 0.9rem;
  color: #8b949e;
  line-height: 1.5;
  margin-bottom: 16px;
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
  text-decoration: underline;
}

/* RESPONSIVE */
@media (max-width: 1024px) {
  .featured-grid {
    grid-template-columns: 1fr;
    gap: 48px;
  }
  .featured-service {
    padding: 60px 32px;
    border-radius: 24px 24px 0 0;
  }
  .services-bottom-grid {
    grid-template-columns: 1fr;
    gap: 0;
    border-top: none;
  }
  .grid-item {
    padding: 40px 32px;
    border-left: none !important;
    border-bottom: 1px solid rgba(255, 255, 255, 0.1);
  }
  .grid-item:first-child {
    padding-top: 40px;
  }
  .grid-item:last-child {
    border-bottom: none;
  }
}

@media (max-width: 768px) {
  .main-container {
    padding: 0 16px;
  }
  .featured-service {
    padding: 48px 20px;
    border-radius: 24px 24px 0 0;
  }
  .services-bottom-grid {
    border-radius: 0;
  }
  .featured-title {
    font-size: 1.85rem;
  }
  .featured-desc {
    font-size: 1.05rem;
  }
  .grid-item {
    padding: 32px 20px;
  }
  .outer-card {
    padding: 16px;
  }
  .inner-header {
    padding: 10px 12px;
  }
  .code-diff {
    font-size: 11px;
  }
}
</style>
