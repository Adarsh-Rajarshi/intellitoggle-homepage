<template>
  <nav class="fixed top-0 left-0 right-0 z-50 bg-white shadow-sm">
    <div class="max-w-7xl mx-auto px-4 sm:px-6 lg:px-8">
      <div class="flex items-center justify-between h-16">

        <!-- logo -->
        <div class="flex items-center gap-2">
          <svg width="28" height="28" viewBox="0 0 28 28" fill="none" xmlns="http://www.w3.org/2000/svg">
            <rect x="4" y="2" width="4" height="22" rx="2" fill="#3B39C7"/>
            <rect x="12" y="2" width="4" height="22" rx="2" fill="#3B39C7"/>
            <rect x="2" y="7" width="11" height="4" rx="2" fill="#3B39C7"/>
          </svg>
          <span class="font-bold text-lg text-[#3B39C7] tracking-tight">IntelliToggle</span>
        </div>

        <!-- desktop links -->
        <div class="hidden md:flex items-center gap-8">
          <a href="#" class="text-gray-600 hover:text-[#3B39C7] text-sm font-medium transition-colors duration-200">Home</a>
          <a href="#about" class="text-gray-600 hover:text-[#3B39C7] text-sm font-medium transition-colors duration-200">About</a>
          <a href="#pricing" class="text-gray-600 hover:text-[#3B39C7] text-sm font-medium transition-colors duration-200">Pricing</a>
        </div>

        <!-- cta -->
        <div class="hidden md:block">
          <a href="#" class="bg-[#F5A623] hover:bg-[#e09a1a] text-white text-sm font-semibold px-5 py-2.5 rounded-lg transition-colors duration-200">
            Start Sandbox
          </a>
        </div>

        <!-- mobile hamburger -->
        <button
          @click="isOpen = !isOpen"
          class="md:hidden p-2 text-gray-600 hover:text-[#3B39C7] transition-colors"
          aria-label="Toggle navigation menu"
        >
          <svg v-if="!isOpen" width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
            <line x1="3" y1="6" x2="21" y2="6"/>
            <line x1="3" y1="12" x2="21" y2="12"/>
            <line x1="3" y1="18" x2="21" y2="18"/>
          </svg>
          <svg v-else width="22" height="22" fill="none" stroke="currentColor" stroke-width="2" stroke-linecap="round">
            <line x1="18" y1="6" x2="6" y2="18"/>
            <line x1="6" y1="6" x2="18" y2="18"/>
          </svg>
        </button>

      </div>
    </div>

    <!-- mobile dropdown -->
    <div v-if="isOpen" class="md:hidden bg-white border-t border-gray-100 px-4 pt-3 pb-5 flex flex-col gap-3">
      <a href="#" class="text-gray-700 text-sm font-medium py-2 border-b border-gray-50">Home</a>
      <a href="#about" class="text-gray-700 text-sm font-medium py-2 border-b border-gray-50">About</a>
      <a href="#pricing" class="text-gray-700 text-sm font-medium py-2 border-b border-gray-50">Pricing</a>
      <a href="#" class="mt-2 bg-[#F5A623] text-white text-sm font-semibold px-5 py-2.5 rounded-lg text-center">
        Start Sandbox
      </a>
    </div>
  </nav>
</template>

<script setup>
const isOpen = ref(false)
</script>