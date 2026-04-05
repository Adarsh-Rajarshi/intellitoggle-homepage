<template>
  <section class="bg-white py-10 px-4 border-b border-gray-100">
    <div class="max-w-5xl mx-auto">
      <p class="text-center text-gray-400 text-sm mb-7">Trusted by various engineering teams</p>
      <div class="flex flex-wrap items-center justify-center gap-8 md:gap-14">

        <!-- amazon aws -->
        <div class="flex items-center gap-2 opacity-60 hover:opacity-100 transition-opacity">
          <svg width="32" height="20" viewBox="0 0 32 20" fill="none">
            <path d="M9 14c-2.5 1.5-6 1.5-8 0" stroke="#FF9900" stroke-width="2" stroke-linecap="round"/>
            <path d="M2 10c0-4 3-7 7-7s7 3 7 7" stroke="#232F3E" stroke-width="2" fill="none"/>
            <rect x="14" y="8" width="5" height="7" rx="1" fill="#232F3E"/>
          </svg>
          <span class="text-sm font-semibold text-gray-700">Amazon Web Services</span>
        </div>

        <!-- microsoft azure -->
        <div class="flex items-center gap-2 opacity-60 hover:opacity-100 transition-opacity">
          <svg width="22" height="22" viewBox="0 0 22 22" fill="none">
            <path d="M2 16L9 2l5 9-4 3 8 2-18 0z" fill="#0078D4"/>
          </svg>
          <span class="text-sm font-semibold text-gray-700">Microsoft Azure</span>
        </div>

        <!-- openfeature -->
        <div class="flex items-center gap-2 opacity-60 hover:opacity-100 transition-opacity">
          <div class="w-5 h-5 rounded bg-[#3B39C7] flex items-center justify-center">
            <span class="text-white text-xs font-bold">O</span>
          </div>
          <span class="text-sm font-semibold text-gray-700">OpenFeature</span>
        </div>

        <!-- dart -->
        <div class="flex items-center gap-2 opacity-60 hover:opacity-100 transition-opacity">
          <svg width="20" height="22" viewBox="0 0 20 22" fill="none">
            <path d="M2 18L2 6L8 2L18 2L18 8L6 20L2 18Z" fill="#00B4AB"/>
          </svg>
          <span class="text-sm font-semibold text-gray-700">Dart</span>
        </div>

      </div>
    </div>
  </section>
</template>