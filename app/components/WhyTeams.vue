<template>
  <section class="bg-gray-50 py-20 px-4">
    <div class="max-w-6xl mx-auto">

      <div class="text-center mb-12">
        <h2 class="text-2xl md:text-4xl font-bold text-gray-900 mb-3">Why Teams Use IntelliToggle</h2>
        <p class="text-gray-400 text-sm max-w-md mx-auto">
          Start your 7-day free sandbox. No credit card needed.
        </p>
      </div>

      <div class="grid md:grid-cols-3 gap-6 mb-10">
        <div v-for="reason in reasons" :key="reason.title"
          class="bg-white rounded-2xl p-6 border border-gray-100 hover:border-[#3B39C7]/20 hover:shadow-md transition-all">
          <div class="w-10 h-10 rounded-xl bg-[#3B39C7]/8 flex items-center justify-center mb-4">
            <span class="text-xl">{{ reason.icon }}</span>
          </div>
          <h3 class="font-bold text-gray-900 text-base mb-2">{{ reason.title }}</h3>
          <p class="text-gray-400 text-sm leading-relaxed">{{ reason.desc }}</p>
        </div>
      </div>

      <div class="text-center">
        <a href="#" class="inline-flex items-center gap-2 bg-[#3B39C7] hover:bg-[#2f2db0] text-white text-sm font-semibold px-7 py-3 rounded-xl transition-colors">
          Start your free trial →
        </a>
      </div>

    </div>
  </section>
</template>

<script setup>
const reasons = [
  {
    icon: '🎯',
    title: 'Why only works natively',
    desc: 'IntelliToggle is the only feature flag platform built ground-up for Dart, ideal for Flutter teams.'
  },
  {
    icon: '🔗',
    title: 'DartStream integration',
    desc: 'Pricing transparency. Pricing is public, no sales call needed. Simple usage-based costs.'
  },
  {
    icon: '🔍',
    title: 'Quickly verify what matters',
    desc: 'Granular rollout strategies. Target specific users, devices or regions with precision.'
  }
]
</script>