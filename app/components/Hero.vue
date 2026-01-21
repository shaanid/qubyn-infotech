<script setup>
import Stars from '~/components/Stars.vue'
</script>

<template>
  <section class="relative min-h-[720px] flex items-center overflow-hidden">

    <!-- ⭐ STARS (VISIBLE NOW) -->
    <Stars />

    <!-- 🌍 HERO IMAGE WRAPPER (POSITION OK, ZOOM FIXED) -->
    <div
      class="
        absolute inset-0
        z-[2]
        translate-x-12 sm:translate-x-24 md:translate-x-52
        scale-105
        transition-transform duration-[1200ms] ease-out
        will-change-transform
      "
    >
      <img
        src="/hero-visual.png"
        alt="Hero Visual"
        class="
          w-full h-full object-cover object-right
          animate-[float_16s_ease-in-out_infinite]
        "
        draggable="false"
      />
    </div>

    <!-- 🌫 GRADIENT OVERLAY -->
    <div
      class="absolute inset-0 z-[3]
             bg-gradient-to-r from-black/90 via-black/55 to-transparent
             transition-opacity duration-[1200ms]"
    ></div>

    <!-- 📝 CONTENT -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-28 w-full">
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
              class="px-5 py-4 rounded-lg text-black w-full sm:w-80
                     focus:outline-none focus:ring-2 focus:ring-purple-500"
            />

            <button
              class="bg-blue-600 hover:bg-blue-500
                     px-6 py-4 rounded-lg font-semibold
                     transition-transform duration-300
                     hover:scale-105"
            >
              Get in Touch
            </button>
          </div>
        </div>

        <div class="hidden md:block"></div>
      </div>
    </div>

    <!-- 🔻 BOTTOM TRANSITION -->
    <div
      class="absolute bottom-0 left-0 right-0 z-[4] h-40
             bg-gradient-to-b from-transparent to-[#0b0730]">
    </div>

  </section>
</template>
