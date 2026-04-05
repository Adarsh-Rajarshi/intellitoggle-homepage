<template>
  <section class="bg-[#0e0c2e] py-20 px-4 relative overflow-hidden">

    <!-- AI background pattern -->
    <div class="absolute inset-0 opacity-5"
      style="background-image: repeating-linear-gradient(0deg, transparent, transparent 40px, rgba(255,255,255,.3) 40px, rgba(255,255,255,.3) 41px), repeating-linear-gradient(90deg, transparent, transparent 40px, rgba(255,255,255,.3) 40px, rgba(255,255,255,.3) 41px);">
    </div>

    <!-- big AI text in background -->
    <div class="absolute right-10 top-10 text-[200px] font-black text-white/[0.03] leading-none select-none hidden lg:block">
      AI
    </div>

    <div class="relative z-10 max-w-6xl mx-auto">

      <!-- coming soon badge -->
      <div class="flex justify-center mb-6">
        <span class="bg-[#F5A623] text-white text-xs font-bold px-3 py-1 rounded-full">Coming Soon</span>
      </div>

      <div class="grid md:grid-cols-2 gap-12 items-start">

        <!-- left -->
        <div>
          <h2 class="text-2xl md:text-4xl font-bold text-white mb-4 leading-snug">
            DartCodeAI That Actually Changes Flagging
          </h2>
          <p class="text-white/50 text-sm leading-relaxed mb-8">
            AI built natively for Dart feature flagging. Zero wrappers, no SDKs built for other languages.
            Everything from one place with full type safety.
          </p>

          <!-- feature list -->
          <div class="space-y-4">
            <div v-for="feat in features" :key="feat.title" class="flex items-start gap-4">
              <div class="w-10 h-10 rounded-xl bg-white/5 border border-white/10 flex items-center justify-center shrink-0">
                <span class="text-lg">{{ feat.icon }}</span>
              </div>
              <div>
                <div class="text-white font-semibold text-sm mb-1">{{ feat.title }}</div>
                <div class="text-white/40 text-xs leading-relaxed">{{ feat.desc }}</div>
              </div>
            </div>
          </div>

          <!-- enterprise early access -->
          <div class="mt-8 border border-white/10 rounded-xl p-4">
            <div class="text-[#F5A623] text-xs font-bold mb-1">Enterprise Only</div>
            <div class="text-white text-sm font-semibold mb-3">Be The First To Try Out Our New AI Features.</div>
            <div class="flex gap-2">
              <input
                type="email"
                placeholder="Enter email address"
                class="flex-1 bg-white/5 border border-white/10 rounded-lg px-3 py-2 text-white text-xs placeholder-white/20 outline-none focus:border-[#3B39C7]/50"
              />
              <button class="bg-[#3B39C7] hover:bg-[#2f2db0] text-white text-xs font-semibold px-4 py-2 rounded-lg transition-colors">
                Get access
              </button>
            </div>
          </div>
        </div>

        <!-- right - ai feature cards -->
        <div class="space-y-3">
          <div v-for="card in aiCards" :key="card.title"
            class="bg-white/5 border border-white/10 rounded-xl p-4 hover:border-[#3B39C7]/40 transition-colors">
            <div class="flex items-start gap-3">
              <div class="w-8 h-8 rounded-lg bg-[#3B39C7]/30 flex items-center justify-center text-sm shrink-0">
                {{ card.icon }}
              </div>
              <div>
                <div class="text-white font-semibold text-sm mb-1">{{ card.title }}</div>
                <div class="text-white/40 text-xs leading-relaxed">{{ card.desc }}</div>
              </div>
            </div>
          </div>
        </div>

      </div>
    </div>
  </section>
</template>

<script setup>
const features = [
  {
    icon: '🚀',
    title: 'Dart-first from the ground up',
    desc: 'Not a JS wrapper. Native Dart SDK with full type safety and tree shaking.'
  },
  {
    icon: '⚡',
    title: 'Real-time flag evaluations',
    desc: 'WebSocket + gRPC streaming. Sub-millisecond updates across all clients.'
  }
]

const aiCards = [
  {
    icon: '🤖',
    title: 'AutoFlag AI (LLM-Assisted Flag Creation)',
    desc: 'Create new flags just by typing what you need. The AI names it, sets rules, and configures targeting for you.'
  },
  {
    icon: '📈',
    title: 'SmartRamp AI (AI-Driven Rollout Optimization)',
    desc: 'Rollouts that adjust themselves. AI expands, pauses, or rolls back based on real-time metrics.'
  },
  {
    icon: '🔍',
    title: 'ExplainFlags AI (LLM Root-Cause + Insights)',
    desc: 'Understand issues instantly with AI-generated, plain-language insights tied to your flags.'
  },
  {
    icon: '🎯',
    title: 'AutoSegment AI (Behavioral Segmentation)',
    desc: 'Target the right users automatically. AI builds segments from live behavior — no manual rules.'
  }
]
</script>