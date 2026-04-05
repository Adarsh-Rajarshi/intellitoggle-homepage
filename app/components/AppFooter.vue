<template>
  <footer class="bg-[#f5f5fa] py-14 px-4 border-t border-gray-200">
    <div class="max-w-6xl mx-auto">

      <div class="grid grid-cols-1 md:grid-cols-4 gap-10 mb-10">

        <!-- brand col -->
        <div class="md:col-span-1">
          <div class="flex items-center gap-2 mb-4">
            <svg width="24" height="24" viewBox="0 0 28 28" fill="none">
              <rect x="4" y="2" width="4" height="22" rx="2" fill="#3B39C7"/>
              <rect x="12" y="2" width="4" height="22" rx="2" fill="#3B39C7"/>
              <rect x="2" y="7" width="11" height="4" rx="2" fill="#3B39C7"/>
            </svg>
            <span class="font-bold text-gray-900">Intelli Toggle</span>
          </div>
          <p class="text-gray-400 text-xs leading-relaxed mb-4">
            IntelliToggle is built by AORTEM, a company focused on powering scalable,
            multi-platform developer tools.
          </p>
          <!-- github icon -->
          <a href="#" class="inline-flex items-center justify-center w-8 h-8 rounded-full border border-gray-200 hover:border-[#3B39C7] transition-colors">
            <svg width="14" height="14" fill="currentColor" class="text-gray-500" viewBox="0 0 24 24">
              <path d="M12 2C6.477 2 2 6.484 2 12.017c0 4.425 2.865 8.18 6.839 9.504.5.092.682-.217.682-.483 0-.237-.008-.868-.013-1.703-2.782.605-3.369-1.343-3.369-1.343-.454-1.158-1.11-1.466-1.11-1.466-.908-.62.069-.608.069-.608 1.003.07 1.531 1.032 1.531 1.032.892 1.53 2.341 1.088 2.91.832.092-.647.35-1.088.636-1.338-2.22-.253-4.555-1.113-4.555-4.951 0-1.093.39-1.988 1.029-2.688-.103-.253-.446-1.272.098-2.65 0 0 .84-.27 2.75 1.026A9.564 9.564 0 0112 6.844c.85.004 1.705.115 2.504.337 1.909-1.296 2.747-1.027 2.747-1.027.546 1.379.202 2.398.1 2.651.64.7 1.028 1.595 1.028 2.688 0 3.848-2.339 4.695-4.566 4.943.359.309.678.92.678 1.855 0 1.338-.012 2.419-.012 2.747 0 .268.18.58.688.482A10.019 10.019 0 0022 12.017C22 6.484 17.522 2 12 2z"/>
            </svg>
          </a>
        </div>

        <!-- company links -->
        <div>
          <h4 class="text-gray-900 font-semibold text-sm mb-4">Company</h4>
          <ul class="space-y-3">
            <li><a href="#pricing" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Pricing</a></li>
            <li><a href="#" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Doc</a></li>
            <li><a href="#about" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">About Us</a></li>
          </ul>
        </div>

        <!-- resources links -->
        <div>
          <h4 class="text-gray-900 font-semibold text-sm mb-4">Resources</h4>
          <ul class="space-y-3">
            <li><a href="#" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Why IntelliToggle is different</a></li>
            <li><a href="#" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Customer Support</a></li>
            <li><a href="#" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Terms & conditions</a></li>
            <li><a href="#" class="text-gray-400 text-sm hover:text-[#3B39C7] transition-colors">Privacy Policy</a></li>
          </ul>
        </div>

        <!-- newsletter -->
        <div>
          <h4 class="text-gray-900 font-semibold text-sm mb-4">Subscribe to Newsletter</h4>
          <div class="flex gap-2">
            <input
              v-model="email"
              type="email"
              placeholder="Enter email address"
              class="flex-1 border border-gray-200 rounded-lg px-3 py-2 text-xs text-gray-700 placeholder-gray-300 outline-none focus:border-[#3B39C7] transition-colors min-w-0"
            />
            <button
              @click="subscribe"
              class="bg-[#1e1b4b] hover:bg-[#3B39C7] text-white text-xs font-semibold px-4 py-2 rounded-lg transition-colors shrink-0"
            >
              Join
            </button>
          </div>
          <p v-if="subscribed" class="text-green-500 text-xs mt-2">Thanks for subscribing! ✓</p>
        </div>

      </div>

      <!-- bottom bar -->
      <div class="border-t border-gray-200 pt-6 flex flex-col md:flex-row items-center justify-between gap-3">
        <span class="text-gray-400 text-xs">© 2024 AORTEM. All rights reserved.</span>
        <span class="text-gray-400 text-xs">Built with ❤️ for Dart developers</span>
      </div>

    </div>
  </footer>
</template>

<script setup>
const email = ref('')
const subscribed = ref(false)

function subscribe() {
  if (email.value) {
    subscribed.value = true
    email.value = ''
    setTimeout(() => subscribed.value = false, 3000)
  }
}
</script>