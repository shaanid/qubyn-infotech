<script setup>
import Stars from "~/components/Stars.vue";
</script>

<template>
  <section class="relative min-h-[720px] flex items-center overflow-hidden">
    <!-- 🎭 BACKGROUND MASK WRAPPER -->
    <div
      class="absolute inset-0 z-[1] pointer-events-none [mask-image:linear-gradient(to_bottom,black_80%,transparent)]"
    >
      <!-- 🌌 VISUAL SCENE -->
      <div class="absolute inset-0">
        <div class="relative w-full h-full">
          <!-- 🌍 GLOBE (STATIC) -->
          <img
            src="/globe.png"
            alt="Globe"
            draggable="false"
            class="absolute left-1/2 -translate-x-1/2 bottom-[-10%] w-[80vw] lg:left-auto lg:right-[14%] lg:translate-x-0 lg:bottom-[-6%] lg:w-[640px] sm:w-[520px] md:w-[580px] drop-shadow-[0_0_55px_rgba(168,85,247,0.6)]"
          />

          <!-- 👨‍🚀 ASTRONAUT (SPACE FLOAT) -->
          <img
            src="/astronaut.png"
            alt="Astronaut"
            draggable="false"
            class="hidden sm:block absolute right-[6%] bottom-[6%] w-[260px] sm:w-[290px] md:w-[320px] animate-[float_22s_ease-in-out_infinite] z-10"
          />
        </div>
      </div>

      <!-- 🌫 LEFT DARK GRADIENT -->
      <div
        class="absolute inset-0 z-[2] bg-gradient-to-r from-black/90 via-black/60 to-transparent"
      ></div>

      <!-- ⭐ STARS -->
      <Stars />
    </div>

    <!-- 📝 HERO CONTENT -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-32 w-full">
      <div class="grid md:grid-cols-2 gap-16 items-center">
        <div>
          <h1 class="text-6xl md:text-7xl font-extrabold leading-tight mb-6">
            Let’s build <br />
            <span class="text-purple-400">from here</span>
          </h1>

          <p class="text-xl text-gray-300 max-w-lg mb-10">
            Qubyn Infotech delivers secure, scalable, and high-performance
            software solutions designed for growth-driven companies.
          </p>

          <div class="flex flex-col sm:flex-row gap-4">
            <input
              type="email"
              placeholder="Enter your email"
              class="px-5 py-4 rounded-xl bg-white/5 backdrop-blur-md border border-white/10 text-white w-full sm:w-80 placeholder:text-gray-500 focus:outline-none focus:ring-2 focus:ring-purple-500/50 focus:border-purple-500/50"
            />

            <button
              class="bg-purple-600 hover:bg-purple-500 px-6 py-3 rounded-lg"
            >
              Get in Touch
            </button>
          </div>
        </div>

        <div class="hidden md:block"></div>
      </div>
    </div>
  </section>
</template>
