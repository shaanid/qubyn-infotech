<script setup>
import Stars from "~/components/Stars.vue";
import AboutSection from "~/components/AboutSection.vue";
</script>

<template>
  <div class="relative pt-32 pb-20 px-6 min-h-screen bg-[#020408]">
    <Stars />

    <!-- Hero Section -->
    <section class="relative z-10 max-w-4xl mx-auto text-center mb-20">
      <h1 class="text-5xl md:text-6xl font-extrabold mb-8 tracking-tight">
        Innovating for the <span class="text-purple-400">Future</span>
      </h1>
      <p class="text-xl text-gray-300 leading-relaxed max-w-3xl mx-auto">
        At Qubyn Infotech, we believe technology is the catalyst for growth. We
        build robust, scalable, and forward-thinking software solutions that
        empower businesses to navigate the digital era with confidence.
      </p>
    </section>

    <!-- Content Components -->
    <AboutSection />
  </div>
</template>
