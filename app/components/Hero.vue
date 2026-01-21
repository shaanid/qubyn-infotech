<template>
  <section
    class="relative overflow-hidden min-h-[700px] flex items-center"
  >
    <!-- Background Image -->
    <div class="absolute inset-0 z-0">
      <img
        src="/hero-visual.png"
        alt="Hero background"
        class="w-full h-full object-cover object-right md:object-center"
      />
      <!-- Dark overlay for readability -->
      <div
        class="absolute inset-0 bg-gradient-to-r from-black/90 via-black/60 to-transparent"
      ></div>
    </div>

    <!-- Content -->
    <div class="relative z-10 max-w-7xl mx-auto px-6 py-28 w-full">
      <div class="grid md:grid-cols-2 gap-12">
        <div class="max-w-2xl">
          <h1 class="text-5xl md:text-7xl font-extrabold leading-tight mb-6">
            Let’s build <br />
            <span class="text-purple-400">from here</span>
          </h1>

          <p class="text-xl text-gray-300 max-w-lg mb-10 leading-relaxed">
            Qubyn Infotech delivers secure, scalable, and high-performance
            software solutions designed for growth-driven companies.
          </p>

          <div class="flex flex-col sm:flex-row gap-4">
            <input
              type="email"
              placeholder="Enter your email"
              class="px-5 py-4 rounded-lg text-black w-full sm:w-80 focus:outline-none"
            />
            <button
              class="bg-purple-600 hover:bg-purple-500 px-4 py-2 rounded-lg transition"
            >
              Get in Touch
            </button>
          </div>
        </div>

        <!-- empty column to push text left -->
        <div class="hidden md:block"></div>
      </div>
    </div>

    <!-- BOTTOM BLEND (THIS IS THE LINE YOU ASKED ABOUT) -->
    <div
      class="absolute bottom-0 left-0 right-0 h-32 bg-gradient-to-b from-transparent to-[#0b0730]"
    ></div>
  </section>
</template>
