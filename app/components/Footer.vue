<template>
  <footer class="footer-root">
    <div class="footer-glow"></div>

    <div class="main-container">
      <div class="footer-grid">
        <!-- Brand Column -->
        <div class="brand-col">
          <div class="footer-logo">
            <span class="logo-text"
              >Qubyn Infotech Pvt Ltd<span class="highlight">.</span></span
            >
          </div>
          <p class="brand-desc">
            Empowering global enterprises with high-performance digital products
            and engineering excellence. We build for the future of the web.
          </p>
          <div class="social-links">
            <a href="#" class="social-icon" aria-label="Github"
              ><Github :size="18"
            /></a>
            <a href="#" class="social-icon" aria-label="Twitter"
              ><Twitter :size="18"
            /></a>
            <a href="#" class="social-icon" aria-label="Linkedin"
              ><Linkedin :size="18"
            /></a>
          </div>
        </div>

        <!-- Links Columns -->
        <div class="links-group">
          <div class="links-col">
            <h4 class="col-title">Solutions</h4>
            <ul class="footer-links">
              <li><a href="#">Web Engineering</a></li>
              <li><a href="#">AI & Cloud</a></li>
              <li><a href="#">Mobile Apps</a></li>
              <li><a href="#">UI/UX Design</a></li>
            </ul>
          </div>

          <div class="links-col">
            <h4 class="col-title">Company</h4>
            <ul class="footer-links">
              <li><NuxtLink to="/about">About Us</NuxtLink></li>
              <li><NuxtLink to="/services">Services</NuxtLink></li>
              <li><a href="#">Projects</a></li>
              <li><a href="#">Careers</a></li>
            </ul>
          </div>

          <div class="links-col">
            <h4 class="col-title">Resources</h4>
            <ul class="footer-links">
              <li><a href="#">Documentation</a></li>
              <li><a href="#">Help Center</a></li>
              <li><a href="#">Privacy Policy</a></li>
              <li><a href="#">Terms of Service</a></li>
            </ul>
          </div>
        </div>
      </div>

      <div class="footer-bottom">
        <div class="copyright">
          © {{ new Date().getFullYear() }} Qubyn Infotech. Crafted with
          precision.
        </div>
      </div>
    </div>
  </footer>
</template>

<script setup>
import { Github, Twitter, Linkedin } from "lucide-vue-next";
</script>

<style scoped>
.footer-root {
  background: #020408;
  padding: 100px 0 40px;
  position: relative;
  overflow: hidden;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.footer-glow {
  position: absolute;
  bottom: -100px;
  left: 50%;
  transform: translateX(-50%);
  width: 800px;
  height: 400px;
  background: radial-gradient(
    circle,
    rgba(139, 92, 246, 0.05) 0%,
    transparent 70%
  );
  filter: blur(80px);
  z-index: 0;
}

.main-container {
  max-width: 1216px;
  margin: 0 auto;
  padding: 0 32px;
  position: relative;
  z-index: 1;
}

.footer-grid {
  display: grid;
  grid-template-columns: 1fr 2fr;
  gap: 100px;
  margin-bottom: 80px;
}

/* Brand Column */
.brand-col {
  max-width: 320px;
}

.footer-logo {
  margin-bottom: 24px;
}

.logo-text {
  font-size: 1.5rem;
  font-weight: 800;
  color: #fff;
  letter-spacing: -0.02em;
}

.logo-text .highlight {
  color: #bc8cff;
}

.brand-desc {
  color: #8b949e;
  line-height: 1.6;
  font-size: 0.95rem;
  margin-bottom: 32px;
}

.social-links {
  display: flex;
  gap: 16px;
}

.social-icon {
  width: 40px;
  height: 40px;
  background: rgba(255, 255, 255, 0.03);
  border: 1px solid rgba(255, 255, 255, 0.05);
  border-radius: 10px;
  display: flex;
  align-items: center;
  justify-content: center;
  color: #8b949e;
  transition: all 0.3s ease;
}

.social-icon:hover {
  background: rgba(188, 140, 255, 0.1);
  color: #bc8cff;
  border-color: rgba(188, 140, 255, 0.2);
  transform: translateY(-2px);
}

/* Links Group */
.links-group {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 40px;
}

.col-title {
  color: #fff;
  font-size: 0.9rem;
  font-weight: 700;
  text-transform: uppercase;
  letter-spacing: 0.1em;
  margin-bottom: 24px;
}

.footer-links {
  list-style: none;
  padding: 0;
}

.footer-links li {
  margin-bottom: 12px;
}

.footer-links a {
  color: #8b949e;
  text-decoration: none;
  font-size: 0.95rem;
  transition: color 0.2s ease;
}

.footer-links a:hover {
  color: #fff;
}

/* Footer Bottom */
.footer-bottom {
  padding-top: 40px;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.copyright {
  color: #484f58;
  font-size: 0.85rem;
}

.bottom-tag {
  color: #8b949e;
  font-size: 0.85rem;
  display: flex;
  align-items: center;
  gap: 8px;
}

.status-dot {
  width: 8px;
  height: 8px;
  background: #238636;
  border-radius: 50%;
  box-shadow: 0 0 10px #238636;
}

/* Responsive */
@media (max-width: 1024px) {
  .footer-grid {
    grid-template-columns: 1fr;
    gap: 60px;
  }
  .brand-col {
    max-width: 100%;
    text-align: center;
    display: flex;
    flex-direction: column;
    align-items: center;
  }
}

@media (max-width: 768px) {
  .links-group {
    grid-template-columns: 1fr;
    text-align: center;
  }
  .footer-bottom {
    flex-direction: column;
    gap: 20px;
    text-align: center;
  }
}
</style>
