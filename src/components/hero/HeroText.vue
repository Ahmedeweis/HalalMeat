<script setup>
defineProps({
  badgeText: String,
  title: String,
  subtitle: String,
})
</script>

<template>
  <div class="flex flex-col items-start text-white space-y-6 lg:space-y-8 z-10 animate-fade-in-up">
    <!-- Badge -->
    <div class="inline-flex items-center px-4 py-1.5 rounded-full bg-secondary/10 border border-secondary/30 backdrop-blur-sm">
      <span class="text-secondary font-bold text-xs uppercase tracking-wider animate-pulse">{{ badgeText || 'Best Quality Halal Products' }}</span>
    </div>

    <!-- Headache -->
    <h1 class="text-5xl md:text-6xl lg:text-7xl font-extrabold leading-[1.1] tracking-tight">
      Halal Meat & <br>
      Grocery Delivery <br>
      Service In <span class="relative inline-block text-secondary">
        America
        <svg class="absolute -bottom-2 left-0 w-full h-3 text-secondary" viewBox="0 0 100 10" preserveAspectRatio="none">
          <path d="M0 5 Q 50 10 100 5" stroke="currentColor" stroke-width="3" fill="none" />
        </svg>
      </span>
    </h1>

    <!-- Description -->
    <p class="text-lg md:text-xl text-gray-300 max-w-lg leading-relaxed">
      Energistically harness progressive technology for top-line catalysts for change. Rapidly monetize one-to-one e-markets for high standards.
    </p>

    <!-- Build CTA -->
    <div class="flex items-center gap-4 pt-4">
      <button class="group bg-secondary hover:bg-white hover:text-secondary text-white font-bold py-4 px-10 rounded shadow-lg shadow-orange-500/20 transition-all duration-300 transform hover:-translate-y-1 flex items-center gap-2">
        Shop Now
        <svg class="w-5 h-5 transition-transform group-hover:translate-x-1" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
        </svg>
      </button>

      <!-- Optional Trust text or secondary link -->
      <!-- Only if needed -->
    </div>
  </div>
</template>

<style scoped>
.animate-fade-in-up {
  animation: fade-in-up 0.8s ease-out forwards;
}

@keyframes fade-in-up {
  from {
    opacity: 0;
    transform: translateY(20px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
