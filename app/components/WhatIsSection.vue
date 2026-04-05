<template>
  <section id="about" class="bg-white py-20 px-4">
    <div class="max-w-6xl mx-auto">

      <div class="grid md:grid-cols-2 gap-12 items-center">

        <!-- left text -->
        <div>
          <h2 class="text-2xl md:text-4xl font-bold text-gray-900 mb-5">
            What is IntelliToggle?
          </h2>
          <p class="text-gray-500 text-sm leading-relaxed mb-4">
            IntelliToggle is a "Dart-Powered" feature flag that lets you turn features on/off instantly
            in your application without redeploying code.
          </p>
          <p class="text-gray-500 text-sm leading-relaxed mb-6">
            It allows you to control roll-outs, run experiments, and fix bugs faster.
          </p>

          <div class="space-y-3 mb-8">
            <div class="flex items-start gap-3">
              <div class="w-5 h-5 rounded-full bg-[#3B39C7]/10 flex items-center justify-center mt-0.5 shrink-0">
                <svg width="10" height="10" viewBox="0 0 10 10" fill="none">
                  <path d="M2 5l2 2 4-4" stroke="#3B39C7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <span class="text-gray-600 text-sm">Toggle new features without app updates</span>
            </div>
            <div class="flex items-start gap-3">
              <div class="w-5 h-5 rounded-full bg-[#3B39C7]/10 flex items-center justify-center mt-0.5 shrink-0">
                <svg width="10" height="10" viewBox="0 0 10 10" fill="none">
                  <path d="M2 5l2 2 4-4" stroke="#3B39C7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <span class="text-gray-600 text-sm">Roll out to specific users or regions</span>
            </div>
            <div class="flex items-start gap-3">
              <div class="w-5 h-5 rounded-full bg-[#3B39C7]/10 flex items-center justify-center mt-0.5 shrink-0">
                <svg width="10" height="10" viewBox="0 0 10 10" fill="none">
                  <path d="M2 5l2 2 4-4" stroke="#3B39C7" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
                </svg>
              </div>
              <span class="text-gray-600 text-sm">Instantly rollback when needed</span>
            </div>
          </div>

          <!-- benefits label -->
          <div class="bg-gray-50 rounded-xl p-4 inline-block">
            <span class="text-xs font-semibold text-gray-400 uppercase tracking-wide">Benefits</span>
          </div>
        </div>

        <!-- right - chart mockup -->
        <div class="bg-[#f8f8ff] rounded-2xl p-6 border border-gray-100">
          <div class="flex items-center justify-between mb-4">
            <span class="text-xs font-semibold text-gray-500">Flag Activity</span>
            <span class="text-xs text-gray-400">Last 7 days</span>
          </div>
          <!-- fake bar chart -->
          <div class="flex items-end gap-2 h-28">
            <div v-for="(h, i) in bars" :key="i"
              class="flex-1 rounded-t-md transition-all"
              :class="i === 4 ? 'bg-[#3B39C7]' : 'bg-[#3B39C7]/20'"
              :style="`height: ${h}%`"
            ></div>
          </div>
          <div class="flex justify-between mt-2">
            <span v-for="d in ['M','T','W','T','F','S','S']" :key="d" class="text-xs text-gray-400 flex-1 text-center">{{d}}</span>
          </div>

          <div class="mt-5 pt-4 border-t border-gray-100 flex items-center justify-between">
            <div>
              <div class="text-xl font-bold text-gray-900">+42%</div>
              <div class="text-xs text-gray-400">flag evaluations</div>
            </div>
            <div>
              <div class="text-xl font-bold text-green-500">99.9%</div>
              <div class="text-xs text-gray-400">uptime</div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
// just some fake bar heights for the chart
const bars = [40, 55, 35, 70, 90, 60, 45]
</script>