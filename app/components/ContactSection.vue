<template>
  <div
    id="contact"
    class="relative py-32 px-6 bg-[#020408] border-t border-white/5"
  >
    <div class="relative z-10 max-w-7xl mx-auto">
      <div class="text-center mb-16">
        <h2 class="text-4xl md:text-5xl font-extrabold mb-6">
          Get in <span class="text-purple-400">Touch</span>
        </h2>
        <p class="text-xl text-gray-300">
          Have a project in mind? We'd love to hear from you.
        </p>
      </div>

      <div class="grid lg:grid-cols-2 gap-12 lg:gap-20 items-start">
        <!-- Contact Info -->
        <div>
          <h3 class="text-2xl font-bold mb-8">Contact Information</h3>
          <div class="space-y-6">
            <div class="glass-card p-6 flex items-start gap-4">
              <div
                class="w-10 h-10 rounded-full bg-purple-500/10 flex items-center justify-center flex-shrink-0 text-purple-400"
              >
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z"
                  />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-white mb-1">Email Us</h4>
                <p class="text-gray-400">hello@qubyn.com</p>
                <p class="text-gray-400">support@qubyn.com</p>
              </div>
            </div>

            <div class="glass-card p-6 flex items-start gap-4">
              <div
                class="w-10 h-10 rounded-full bg-blue-500/10 flex items-center justify-center flex-shrink-0 text-blue-400"
              >
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z"
                  />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-white mb-1">Call Us</h4>
                <p class="text-gray-400">+1 (555) 123-4567</p>
                <p class="text-gray-400">Mon-Fri from 9am to 6pm</p>
              </div>
            </div>

            <div class="glass-card p-6 flex items-start gap-4">
              <div
                class="w-10 h-10 rounded-full bg-pink-500/10 flex items-center justify-center flex-shrink-0 text-pink-400"
              >
                <svg
                  class="w-5 h-5"
                  fill="none"
                  stroke="currentColor"
                  viewBox="0 0 24 24"
                >
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z"
                  />
                  <path
                    stroke-linecap="round"
                    stroke-linejoin="round"
                    stroke-width="2"
                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z"
                  />
                </svg>
              </div>
              <div>
                <h4 class="font-semibold text-white mb-1">Visit Us</h4>
                <p class="text-gray-400">123 Tech Park Avenue</p>
                <p class="text-gray-400">San Francisco, CA 94103</p>
              </div>
            </div>
          </div>
        </div>

        <!-- Contact Form -->
        <div class="glass-card p-8 md:p-10">
          <h3 class="text-2xl font-bold mb-6">Send a Message</h3>
          <form class="space-y-6">
            <div class="grid md:grid-cols-2 gap-6">
              <div>
                <label class="block text-sm font-medium text-gray-400 mb-2"
                  >First Name</label
                >
                <input
                  type="text"
                  class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-purple-500 transition-colors"
                  placeholder="John"
                />
              </div>
              <div>
                <label class="block text-sm font-medium text-gray-400 mb-2"
                  >Last Name</label
                >
                <input
                  type="text"
                  class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-purple-500 transition-colors"
                  placeholder="Doe"
                />
              </div>
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-400 mb-2"
                >Email Address</label
              >
              <input
                type="email"
                class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-purple-500 transition-colors"
                placeholder="john@example.com"
              />
            </div>

            <div>
              <label class="block text-sm font-medium text-gray-400 mb-2"
                >Message</label
              >
              <textarea
                rows="4"
                class="w-full bg-white/5 border border-white/10 rounded-lg px-4 py-3 text-white focus:outline-none focus:border-purple-500 transition-colors"
                placeholder="Tell us about your project..."
              ></textarea>
            </div>

            <button
              type="button"
              class="w-full bg-purple-600 hover:bg-purple-500 text-white font-semibold py-4 rounded-lg transition-colors shadow-lg shadow-purple-600/30"
            >
              Send Message
            </button>
          </form>
        </div>
      </div>
    </div>
  </div>
</template>
