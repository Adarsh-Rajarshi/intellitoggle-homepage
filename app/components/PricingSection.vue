<template>
  <section id="pricing" class="bg-white py-20 px-4">
    <div class="max-w-6xl mx-auto">

      <div class="text-center mb-12">
        <h2 class="text-2xl md:text-4xl font-bold text-gray-900 mb-3">Plans Built For Every Stage Of Growth</h2>
        <p class="text-gray-400 text-sm">Start for free, scale as your team grows.</p>
      </div>

      <div class="grid md:grid-cols-3 gap-6 mb-8">
        <div v-for="plan in plans" :key="plan.name"
          class="rounded-2xl border p-6 flex flex-col relative"
          :class="plan.popular
            ? 'bg-[#1e1b4b] border-[#3B39C7] shadow-2xl shadow-[#3B39C7]/20'
            : 'bg-white border-gray-200'"
        >
          <!-- popular badge -->
          <div v-if="plan.popular" class="absolute -top-3 left-1/2 -translate-x-1/2">
            <span class="bg-[#F5A623] text-white text-xs font-bold px-4 py-1 rounded-full">Popular</span>
          </div>

          <!-- plan header -->
          <div class="mb-5">
            <!-- spinner icon -->
            <div class="w-8 h-8 mb-3">
              <svg viewBox="0 0 32 32" fill="none" width="32" height="32">
                <circle cx="16" cy="16" r="12" stroke="#3B39C7" stroke-width="2" stroke-dasharray="4 4"/>
                <circle cx="16" cy="16" r="5" fill="#3B39C7"/>
              </svg>
            </div>

            <div class="flex items-start justify-between">
              <span class="font-bold" :class="plan.popular ? 'text-white' : 'text-gray-900'">{{ plan.name }}</span>
              <span class="text-xs font-medium px-2 py-0.5 rounded-full border"
                :class="plan.popular ? 'border-white/20 text-white/60' : 'border-gray-200 text-gray-400'">
                Billed annually
              </span>
            </div>

            <div class="mt-3">
              <span class="font-extrabold text-3xl" :class="plan.popular ? 'text-white' : 'text-gray-900'">
                {{ plan.price }}
              </span>
              <span v-if="plan.period" class="text-sm ml-1" :class="plan.popular ? 'text-white/50' : 'text-gray-400'">
                /month
              </span>
            </div>
          </div>

          <!-- features -->
          <ul class="space-y-2.5 flex-1 mb-6">
            <li v-for="feat in plan.features" :key="feat" class="flex items-start gap-2.5">
              <svg width="14" height="14" viewBox="0 0 14 14" fill="none" class="mt-0.5 shrink-0">
                <path d="M2.5 7l3 3 6-6" :stroke="plan.popular ? '#818cf8' : '#3B39C7'" stroke-width="1.5" stroke-linecap="round" stroke-linejoin="round"/>
              </svg>
              <span class="text-xs leading-relaxed" :class="plan.popular ? 'text-white/70' : 'text-gray-500'">{{ feat }}</span>
            </li>
          </ul>

          <!-- button -->
          <button class="w-full py-2.5 rounded-xl text-sm font-semibold transition-colors"
            :class="plan.popular
              ? 'bg-white text-[#1e1b4b] hover:bg-gray-100'
              : 'border border-gray-200 text-gray-700 hover:border-[#3B39C7] hover:text-[#3B39C7]'"
          >
            Subscribe
          </button>
        </div>
      </div>

      <!-- view full comparison -->
      <div class="text-center mb-14">
        <button
          @click="showTable = !showTable"
          class="border border-gray-200 text-gray-600 text-sm font-medium px-6 py-2.5 rounded-xl hover:border-[#3B39C7] hover:text-[#3B39C7] transition-colors"
        >
          {{ showTable ? 'Hide' : 'View' }} full price comparison
        </button>
      </div>

      <!-- comparison table (accordion!) -->
      <div v-if="showTable" class="overflow-x-auto rounded-2xl border border-gray-100 shadow-sm">
        <table class="w-full text-sm">
          <thead>
            <tr class="bg-[#1e1b4b]">
              <th class="text-left text-white font-bold px-5 py-4">Features</th>
              <th class="text-center text-white font-semibold px-4 py-4">Standard</th>
              <th class="text-center text-white font-semibold px-4 py-4">Enhanced</th>
              <th class="text-center text-white font-semibold px-4 py-4">Enterprise</th>
            </tr>
          </thead>
          <tbody>
            <tr v-for="(row, i) in tableRows" :key="row.feature"
              class="border-t border-gray-100"
              :class="i % 2 === 0 ? 'bg-white' : 'bg-gray-50/50'"
            >
              <td class="px-5 py-3 text-gray-700 text-xs">{{ row.feature }}</td>
              <td class="px-4 py-3 text-center text-xs text-gray-500">{{ row.standard }}</td>
              <td class="px-4 py-3 text-center text-xs text-gray-500">{{ row.enhanced }}</td>
              <td class="px-4 py-3 text-center text-xs text-gray-500">{{ row.enterprise }}</td>
            </tr>
          </tbody>
          <tfoot>
            <tr class="bg-[#1e1b4b]">
              <td class="px-5 py-3 text-white font-bold text-sm">Price</td>
              <td class="px-4 py-3 text-center text-white font-bold">$10</td>
              <td class="px-4 py-3 text-center text-white font-bold">$149</td>
              <td class="px-4 py-3 text-center text-white font-bold">Custom</td>
            </tr>
          </tfoot>
        </table>
      </div>

      <!-- sandbox cta -->
      <div class="mt-10 bg-gray-50 border border-gray-100 rounded-2xl p-8 flex flex-col md:flex-row items-center justify-between gap-5">
        <div>
          <h3 class="font-bold text-gray-900 text-lg mb-1">Start your 7-days free Sandbox Plan</h3>
          <p class="text-gray-400 text-sm">Join over 1,000+ startups already growing with IntelliToggle.</p>
        </div>
        <div class="flex gap-3 shrink-0">
          <a href="#" class="bg-[#1e1b4b] hover:bg-[#2f2db0] text-white text-sm font-semibold px-5 py-2.5 rounded-lg transition-colors">
            Get Started
          </a>
          <a href="#" class="border border-gray-200 text-gray-700 hover:border-gray-300 text-sm font-semibold px-5 py-2.5 rounded-lg transition-colors">
            Learn More
          </a>
        </div>
      </div>

    </div>
  </section>
</template>

<script setup>
const showTable = ref(false)

const plans = [
  {
    name: 'Standard Plan',
    price: '$10',
    period: true,
    popular: false,
    features: [
      'Core Feature Flags API',
      'Targeting Rules Engine',
      'Percentage Rollouts',
      'Flutter Client SDK',
      'Kill Switch / Instant Rollback',
      'Dart Server SDK (OpenFeature)',
      'API Management Access',
      'SDK Caching and Offline Mode'
    ]
  },
  {
    name: 'Enhance Plan',
    price: '$149',
    period: true,
    popular: true,
    features: [
      'Multi-environment support (Dev / Staging / Prod)',
      'Unlimited feature flags and projects',
      'Advanced targeting rules with custom attributes',
      'Environment-specific flags',
      'Real-time streaming updates (WebSocket / gRPC)',
      'Analytics hooks (flag usage tracking)',
      'Built-in A/B testing / experimentation dashboard',
      'Audit logs (90-day retention + export in CSV/JSON)'
    ]
  },
  {
    name: 'Enterprise Plan',
    price: 'Custom',
    period: false,
    popular: false,
    features: [
      'Unlimited API calls',
      'Unlimited audit log retention (1 Years +)',
      'Full access to all SaaS modules',
      'Dedicated customer success manager',
      '24/7 support',
      'Custom SLA (eg. 99.99% uptime, penalty clauses)',
      'White-labeled portal',
      'Optional on-premises deployment (air-gapped/secure hosting)'
    ]
  }
]

const tableRows = [
  { feature: 'Core Feature Flags API', standard: '✓', enhanced: '✓', enterprise: '✓' },
  { feature: 'Targeting Rules Engine', standard: '✓ (basic)', enhanced: '✓ (advanced + custom)', enterprise: '✓' },
  { feature: 'Percentage Rollouts', standard: '✓ (max 10 flags)', enhanced: '✓ (unlimited)', enterprise: '✓' },
  { feature: 'Kill Switch / Instant Rollback', standard: '✓', enhanced: '✓', enterprise: '✓' },
  { feature: 'Multi-Environment Support', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'Unlimited Flags & Projects', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'Analytics Hooks (Flag Metrics)', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'A/B Testing / Experimentation', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'Streaming Flag Updates (Real-Time)', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'Audit Logs (Flag Changes)', standard: '✗', enhanced: '✓ (90 days)', enterprise: '✓ (unlimited)' },
  { feature: 'SSO (SAML)', standard: '✗', enhanced: '✓', enterprise: '✓' },
  { feature: 'Monthly API Calls', standard: '10k', enhanced: '100k', enterprise: 'Unlimited' },
  { feature: 'Log Retention', standard: '7 days', enhanced: '90 days', enterprise: 'Custom' },
  { feature: 'Support SLA', standard: '72 hours', enhanced: '48 hours', enterprise: '24 hours' }
]
</script>