<template>
  <section class="relative py-28 overflow-hidden">
    <!-- Decorative Glows -->
    <div class="absolute top-1/4 left-1/4 w-96 h-96 bg-purple-600/20 rounded-full blur-[120px] -z-10"></div>
    <div class="absolute bottom-1/4 right-1/4 w-96 h-96 bg-blue-600/20 rounded-full blur-[120px] -z-10"></div>

    <div class="max-w-7xl mx-auto px-6 relative z-10">
      <h3 class="text-4xl font-bold text-center mb-16">What we build</h3>

      <div class="grid md:grid-cols-3 gap-8">
        <div class="glass-card p-8">
          <div
            class="w-12 h-12 bg-purple-500/20 rounded-lg flex items-center justify-center mb-6 border border-purple-500/30">
            <svg class="w-6 h-6 text-purple-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M21 12a9 9 0 01-9 9m9-9a9 9 0 00-9-9m9 9H3m9 9a9 9 0 01-9-9m9 9c1.657 0 3-4.03 3-9s-1.343-9-3-9m0 18c-1.657 0-3-4.03-3-9s1.343-9 3-9m-9 9a9 9 0 019-9" />
            </svg>
          </div>
          <h4 class="text-xl font-semibold mb-3">Web Applications</h4>
          <p class="text-gray-300">
            Scalable, secure, modern web platforms.
          </p>
        </div>

        <div class="glass-card p-8">
          <div
            class="w-12 h-12 bg-blue-500/20 rounded-lg flex items-center justify-center mb-6 border border-blue-500/30">
            <svg class="w-6 h-6 text-blue-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M12 18h.01M8 21h8a2 2 0 002-2V5a2 2 0 00-2-2H8a2 2 0 00-2 2v14a2 2 0 002 2z" />
            </svg>
          </div>
          <h4 class="text-xl font-semibold mb-3">Mobile Apps</h4>
          <p class="text-gray-300">
            iOS & Android apps with flawless UX.
          </p>
        </div>

        <div class="glass-card p-8">
          <div
            class="w-12 h-12 bg-indigo-500/20 rounded-lg flex items-center justify-center mb-6 border border-indigo-500/30">
            <svg class="w-6 h-6 text-indigo-400" fill="none" stroke="currentColor" viewBox="0 0 24 24">
              <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                d="M19 11H5m14 0a2 2 0 012 2v6a2 2 0 01-2 2H5a2 2 0 01-2-2v-6a2 2 0 012-2m14 0V9a2 2 0 00-2-2M5 11V9a2 2 0 012-2m0 0V5a2 2 0 012-2h6a2 2 0 012 2v2M7 7h10" />
            </svg>
          </div>
          <h4 class="text-xl font-semibold mb-3">Cloud & DevOps</h4>
          <p class="text-gray-300">
            CI/CD, automation & cloud scale.
          </p>
        </div>
      </div>
    </div>
  </section>
</template>
