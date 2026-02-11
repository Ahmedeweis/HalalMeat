<script setup>
const categories = [
  { id: 1, name: 'Halal Chicken', image: '/categories/chicken.svg' },
  { id: 2, name: 'Fresh Halal Beef', image: '/categories/beef.svg', active: true },
  { id: 3, name: 'Halal Deli', image: '/categories/deli.svg' },
  { id: 4, name: 'Halal Lamb & Goat', image: '/categories/lamb.svg' },
]
</script>

<template>
  <section class="py-20 bg-white dark:bg-bg">
    <div class="container mx-auto px-4 md:px-8 lg:px-16 text-center">
      
      <!-- Section Header -->
      <div class="mb-12 space-y-4">
        <span class="inline-block px-4 py-1.5 rounded-full bg-orange-100 text-secondary font-bold text-xs uppercase tracking-wider">
          Halal Categories
        </span>
        <h2 class="text-3xl md:text-4xl font-bold text-primary dark:text-white">
          What We Offer for You
        </h2>
        <p class="text-gray-500 max-w-2xl mx-auto">
          Energistically harness progressive technology for top-line catalysts for change. Rapidly monetize one-to-one e-markets for high standards.
        </p>
      </div>

      <!-- Categories Grid -->
      <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-8">
        <div v-for="category in categories" :key="category.id" 
             class="group relative bg-white dark:bg-card rounded-xl p-6 shadow-lg hover:shadow-2xl transition-all duration-300 border border-transparent hover:border-secondary flex items-center gap-4 text-left cursor-pointer transform hover:-translate-y-1"
             :class="{ 'bg-primary text-white border-none': category.active }">
          
          <!-- Image Circle -->
          <div class="w-16 h-16 rounded-full flex-shrink-0 bg-gray-100 flex items-center justify-center overflow-hidden border-2 border-white shadow-sm group-hover:scale-110 transition-transform">
             <!-- Placeholder SVG if image fails -->
             <svg v-if="!category.image.endsWith('.png')" class="w-8 h-8 text-gray-400" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 16l4.586-4.586a2 2 0 012.828 0L16 16m-2-2l1.586-1.586a2 2 0 012.828 0L20 14m-6-6h.01M6 20h12a2 2 0 002-2V6a2 2 0 00-2-2H6a2 2 0 00-2 2v12a2 2 0 002 2z" />
             </svg>
             <img v-else :src="category.image" :alt="category.name" class="w-full h-full object-cover">
          </div>

          <!-- Content -->
          <div>
            <h3 class="font-bold text-lg group-hover:text-secondary transition-colors" :class="{ 'text-white group-hover:text-white': category.active, 'text-gray-900 dark:text-white': !category.active }">
              {{ category.name }}
            </h3>
            <a href="#" class="text-xs font-bold uppercase tracking-wide flex items-center gap-1 mt-1 group-hover:gap-2 transition-all" :class="{ 'text-white/80': category.active, 'text-gray-400 group-hover:text-secondary': !category.active }">
              Shop Now
              <svg class="w-3 h-3" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
              </svg>
            </a>
          </div>

          <!-- Active Indicator (Optional) -->
          <div v-if="category.active" class="absolute inset-0 border-2 border-primary rounded-xl pointer-events-none"></div>

        </div>
      </div>

    </div>
  </section>
</template>
