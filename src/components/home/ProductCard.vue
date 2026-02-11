<script setup>
defineProps({
  product: {
    type: Object,
    required: true,
  }
})
</script>

<template>
  <div class="bg-white dark:bg-card border border-gray-100 dark:border-gray-800 rounded-2xl p-4 transition-all duration-300 hover:shadow-xl hover:border-secondary/30 group relative">
    
    <!-- Discount Badge -->
    <div v-if="product.discount" class="absolute top-4 left-4 bg-red-100 text-red-600 text-[10px] font-bold px-2 py-1 rounded">
      {{ product.discount }}% OFF
    </div>

    <!-- Image -->
    <div class="relative h-48 w-full flex items-center justify-center mb-4 overflow-hidden rounded-xl bg-gray-50">
      <img :src="product.image" :alt="product.name" class="h-full object-contain transform group-hover:scale-110 transition-transform duration-500 will-change-transform" />
      
      <!-- Quick Actions (Slide up on hover) -->
      <div class="absolute bottom-2 left-1/2 transform -translate-x-1/2 translate-y-12 group-hover:translate-y-0 transition-transform duration-300 flex gap-2">
        <button class="w-8 h-8 bg-white text-gray-600 rounded-full shadow-md flex items-center justify-center hover:bg-secondary hover:text-white transition-colors" title="Quick View">
           <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 12a3 3 0 11-6 0 3 3 0 016 0z" /><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z" /></svg>
        </button>
        <button class="w-8 h-8 bg-white text-gray-600 rounded-full shadow-md flex items-center justify-center hover:bg-secondary hover:text-white transition-colors" title="Wishlist">
           <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor"><path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4.318 6.318a4.5 4.5 0 000 6.364L12 20.364l7.682-7.682a4.5 4.5 0 00-6.364-6.364L12 7.636l-1.318-1.318a4.5 4.5 0 00-6.364 0z" /></svg>
        </button>
      </div>
    </div>

    <!-- Category -->
    <div class="text-[10px] text-red-500 font-bold uppercase tracking-wide mb-1">{{ product.category }}</div>

    <!-- Title -->
    <h3 class="font-bold text-gray-900 dark:text-white text-sm md:text-base leading-tight mb-2 hover:text-secondary cursor-pointer">
      {{ product.name }}
    </h3>

    <!-- Rating -->
    <div class="flex items-center gap-1 mb-3">
      <div class="flex text-yellow-400 text-xs">
        <span v-for="i in 5" :key="i">★</span>
      </div>
      <span class="text-[10px] text-gray-400">({{ product.reviews }} Reviews)</span>
    </div>

    <!-- Price & Add Button -->
    <div class="flex items-center justify-between mt-auto">
      <div class="flex flex-col">
        <span v-if="product.oldPrice" class="text-xs text-gray-400 line-through">${{ product.oldPrice }}</span>
        <span class="font-bold text-secondary text-lg">${{ product.price }}</span>
      </div>
      
      <button class="w-8 h-8 rounded-full border border-gray-200 text-primary flex items-center justify-center hover:bg-primary hover:text-white transition-colors">
        <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
        </svg>
      </button>
    </div>

  </div>
</template>
