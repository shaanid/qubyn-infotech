<script setup>
import Terminal from "./Terminal.vue";
</script>

<template>
  <div class="dev-section">
    <div class="content-wrapper">
      <!-- TEXT COLUMN -->
      <div class="text-column">
        <h2>Code with precision. Scale with ease.</h2>
        <p class="subtitle">
          Experience a new standard of developer productivity with AI-driven
          tools.
        </p>

        <a href="#" class="explore-link">
          Discover Our World <span class="arrow">›</span>
        </a>

        <div class="accordion-list">
          <div class="accordion-item">
            <span>Intelligent code completion</span>
            <span class="plus">+</span>
          </div>
          <div class="accordion-item">
            <span>Seamless cloud deployment</span>
            <span class="plus">+</span>
          </div>
          <div class="accordion-item">
            <span>Integrated collaborative tools</span>
            <span class="plus">+</span>
          </div>
        </div>
      </div>

      <!-- VISUAL COLUMN -->
      <div class="visual-column">
        <Terminal />
      </div>
    </div>
  </div>
</template>

<style scoped>
.dev-section {
  position: relative;
  width: 100%;
  background: #010409;
  overflow: hidden;
  display: flex;
  justify-content: center;
  padding: 80px 0;
  border-top: 1px solid rgba(255, 255, 255, 0.05);
}

.content-wrapper {
  display: grid;
  grid-template-columns: 1fr 1fr;
  gap: 4rem;
  align-items: center;
  max-width: 1300px;
  width: 100%;
  padding: 4rem 4rem;
  z-index: 1;
}

/* TEXT COLUMN */
.text-column {
  display: flex;
  flex-direction: column;
  gap: 1rem;
  z-index: 2;
  padding-right: 2rem;
}

.text-column h2 {
  font-size: 2rem;
  font-weight: 600;
  color: #ffffff;
  line-height: 1.2;
  margin-bottom: 0.5rem;
  letter-spacing: -0.01em;
}

.subtitle {
  color: #7d8590;
  font-size: 1.125rem;
  line-height: 1.5;
  margin-bottom: 1.5rem;
  max-width: 90%;
}

.explore-link {
  color: #4493f8;
  font-size: 1rem;
  font-weight: 500;
  text-decoration: none;
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  margin-bottom: 2rem;
  transition: all 0.2s ease;
  width: fit-content;
}

.explore-link:hover {
  color: #58a6ff;
  transform: translateX(5px);
}

.arrow {
  font-size: 1.1rem;
  transition: transform 0.2s ease;
}

.explore-link:hover .arrow {
  transform: translateX(3px);
}

/* VISUAL COLUMN */
.visual-column {
  position: relative;
  display: flex;
  justify-content: center;
  align-items: center;
  z-index: 1;
}

/* ACCORDION LIST */
.accordion-list {
  display: flex;
  flex-direction: column;
}

.accordion-item {
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1rem 0;
  border-top: 1px solid #30363d;
  color: #c9d1d9;
  font-size: 1.125rem;
  cursor: pointer;
  transition: color 0.2s ease;
  font-weight: 500;
}

.accordion-item:last-child {
  border-bottom: 1px solid #30363d;
}

.accordion-item:hover {
  color: #ffffff;
}

.plus {
  font-size: 1.5rem;
  color: #bc8cff;
  font-weight: 300;
  transition: all 0.2s ease;
}

.accordion-item:hover .plus {
  color: #d2a8ff;
  transform: scale(1.1);
}

/* RESPONSIVE */
@media (max-width: 1200px) {
  .content-wrapper {
    grid-template-columns: 1fr;
    gap: 3rem;
    padding: 6rem 2rem;
    text-align: center;
  }

  .text-column {
    padding-right: 0;
    align-items: center;
  }

  .subtitle {
    max-width: 100%;
    margin-left: auto;
    margin-right: auto;
  }

  .accordion-list {
    width: 100%;
    max-width: 600px;
    margin: 0 auto;
  }
}

@media (max-width: 768px) {
  .dev-section {
    padding: 2rem 0;
  }

  .content-wrapper {
    padding: 3rem 1.5rem;
    gap: 2.5rem;
  }

  .text-column h2 {
    font-size: 1.75rem;
  }

  .subtitle {
    font-size: 1rem;
    margin-bottom: 1rem;
  }

  .accordion-item {
    font-size: 1rem;
    padding: 0.875rem 0;
  }

  .plus {
    font-size: 1.25rem;
  }
}

@media (max-width: 480px) {
  .text-column h2 {
    font-size: 1.5rem;
  }

  .content-wrapper {
    padding: 2rem 1rem;
  }
}
</style>
