<template>
  <section class="bg-white py-20 px-4">
    <div class="max-w-6xl mx-auto">

      <div class="text-center mb-12">
        <h2 class="text-2xl md:text-4xl font-bold text-gray-900 mb-3">Control & Power-focused</h2>
        <p class="text-gray-400 text-sm max-w-md mx-auto">
          Everything you need to manage, ship and control features with confidence.
        </p>
      </div>

      <!-- 3 screenshot cards -->
      <div class="grid md:grid-cols-3 gap-6">

        <div v-for="item in steps" :key="item.title" class="group">
          <!-- mockup screen -->
          <div class="bg-gray-900 rounded-xl overflow-hidden mb-4 border border-gray-200 group-hover:border-[#3B39C7]/30 transition-colors">
            <div class="flex items-center gap-1.5 px-3 py-2.5 border-b border-white/5">
              <div class="w-2.5 h-2.5 rounded-full bg-red-400/70"></div>
              <div class="w-2.5 h-2.5 rounded-full bg-yellow-400/70"></div>
              <div class="w-2.5 h-2.5 rounded-full bg-green-400/70"></div>
              <div class="ml-2 text-white/20 text-xs">{{ item.url }}</div>
            </div>
            <!-- fake dashboard rows -->
            <div class="p-4 space-y-2">
              <div class="h-3 rounded bg-[#3B39C7]/40 w-3/4"></div>
              <div class="h-2 rounded bg-white/10 w-full"></div>
              <div class="h-2 rounded bg-white/10 w-5/6"></div>
              <div class="mt-3 grid grid-cols-2 gap-2">
                <div class="h-8 rounded bg-[#3B39C7]/20"></div>
                <div class="h-8 rounded bg-white/5"></div>
              </div>
              <div class="h-2 rounded bg-white/10 w-full"></div>
              <div class="h-2 rounded bg-white/10 w-4/5"></div>
              <div class="mt-2 h-6 rounded bg-[#F5A623]/20 w-1/3"></div>
            </div>
          </div>

          <h3 class="font-bold text-gray-900 text-base mb-1">{{ item.title }}</h3>
          <p class="text-gray-400 text-sm mb-3">{{ item.desc }}</p>
          <a href="#" class="inline-flex items-center gap-1 text-[#3B39C7] text-sm font-semibold border border-[#3B39C7]/30 hover:bg-[#3B39C7]/5 px-3 py-1.5 rounded-lg transition-colors">
            View Documentation
          </a>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const steps = [
  {
    title: 'Connect',
    desc: 'Install SDK in your Dart project in 2 mins.',
    url: 'docs.intellitoggle.com'
  },
  {
    title: 'Create Flags',
    desc: 'Define features in IntelliToggle dashboard.',
    url: 'app.intellitoggle.com'
  },
  {
    title: 'Ship & Control',
    desc: 'Flip switches anytime, see instant results.',
    url: 'app.intellitoggle.com'
  }
]
</script>