<template>
  <section class="bg-[#3B39C7] pt-28 pb-16 px-4 relative overflow-hidden min-h-screen flex items-center">

    <!-- dot grid bg -->
    <div
      class="absolute inset-0 opacity-[0.07]"
      style="background-image: radial-gradient(circle, #fff 1px, transparent 1px); background-size: 28px 28px;"
    ></div>

    <div class="relative z-10 max-w-5xl mx-auto w-full text-center">

      <!-- top badge line -->
      <div class="flex items-center justify-center gap-2 flex-wrap mb-5">
        <span class="text-white text-base md:text-lg font-normal">The First</span>
        <span class="bg-[#F5A623] text-white font-bold text-sm px-3 py-1 rounded">Dart-Native</span>
        <span class="text-white text-base md:text-lg font-normal">Feature Flag &</span>
        <span class="text-white text-base md:text-lg font-bold">DartCodeAI</span>
      </div>

      <!-- main heading -->
      <h1 class="text-3xl sm:text-5xl md:text-6xl font-extrabold text-white leading-tight mb-5">
        The First Dart-Native<br class="hidden md:block"/>
        Feature Flag With<br/>
        DartCodeAI
      </h1>

      <p class="text-blue-200 text-sm md:text-base max-w-xl mx-auto mb-8 leading-relaxed">
        Ship faster, control rollouts, and get ready for AI-powered delivery,
        starting at just $1/month for a limited time.
      </p>

      <!-- cta buttons -->
      <div class="flex flex-col sm:flex-row gap-3 justify-center mb-14">
        <a href="#" class="bg-[#F5A623] hover:bg-[#e09a1a] text-white font-bold px-7 py-3 rounded-lg text-sm transition-colors duration-200">
          Start for $1/mo
        </a>
        <a href="#" class="border-2 border-white/60 hover:border-white text-white font-semibold px-7 py-3 rounded-lg text-sm transition-all duration-200">
          Join AI Early Access
        </a>
      </div>

      <!-- dashboard mockup -->
      <div class="bg-[#2a2870]/60 backdrop-blur border border-white/10 rounded-2xl p-3 max-w-3xl mx-auto shadow-2xl">
        <div class="bg-[#12103a] rounded-xl overflow-hidden">
          <!-- fake browser bar -->
          <div class="flex items-center gap-2 px-4 py-3 border-b border-white/10">
            <div class="w-3 h-3 rounded-full bg-red-400/80"></div>
            <div class="w-3 h-3 rounded-full bg-yellow-400/80"></div>
            <div class="w-3 h-3 rounded-full bg-green-400/80"></div>
            <div class="ml-3 bg-white/5 rounded px-3 py-1 text-xs text-white/30 flex-1 max-w-xs">
              app.intellitoggle.com
            </div>
            <div class="ml-auto">
              <span class="bg-[#F5A623] text-white text-xs px-3 py-1 rounded font-medium">Create Flag</span>
            </div>
          </div>

          <!-- dashboard content -->
          <div class="p-4">
            <div class="flex items-center justify-between mb-4">
              <span class="text-white/70 text-sm font-medium">Dashboard</span>
              <div class="flex gap-2">
                <span class="text-white/30 text-xs">Flags</span>
                <span class="text-white/30 text-xs">Projects</span>
                <span class="text-white/30 text-xs">Analytics</span>
              </div>
            </div>

            <div class="grid grid-cols-3 gap-3 mb-4">
              <div class="bg-white/5 rounded-lg p-3">
                <div class="text-white/40 text-xs mb-1">Total Flags</div>
                <div class="text-white font-bold text-xl">392</div>
              </div>
              <div class="bg-white/5 rounded-lg p-3">
                <div class="text-white/40 text-xs mb-1">Active</div>
                <div class="text-white font-bold text-xl">16</div>
              </div>
              <div class="bg-white/5 rounded-lg p-3">
                <div class="text-white/40 text-xs mb-1">Projects</div>
                <div class="text-white font-bold text-xl">10</div>
              </div>
            </div>

            <!-- fake rows -->
            <div class="space-y-2">
              <div v-for="i in 3" :key="i" class="flex items-center justify-between bg-white/5 rounded px-3 py-2">
                <div class="flex items-center gap-2">
                  <div class="w-2 h-2 rounded-full" :class="i === 2 ? 'bg-gray-500' : 'bg-green-400'"></div>
                  <div class="h-2 rounded bg-white/20" :style="`width: ${60 + i * 20}px`"></div>
                </div>
                <div class="h-2 w-12 rounded bg-white/10"></div>
              </div>
            </div>
          </div>
        </div>
      </div>

    </div>
  </section>
</template>