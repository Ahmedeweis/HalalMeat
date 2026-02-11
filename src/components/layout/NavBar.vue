<script setup>
import { ref } from 'vue'

const menuOpen = ref(false)

const navLinks = [
  { name: 'Home+', href: '#' },
  { name: 'About', href: '#' },
  { name: 'Catalog', href: '#', hasDropdown: true },
  { name: 'Shop', href: '#', hasDropdown: true },
  { name: 'Blogs', href: '#' },
  { name: 'Pages', href: '#', hasDropdown: true },
]
</script>

<template>
  <nav class="absolute top-0 left-0 w-full z-50 text-white py-6 px-4 md:px-8 lg:px-16 flex items-center justify-between">
    <!-- Logo -->
    <a href="/" class="flex items-center gap-2 group">
      <!-- Custom SVG Logo -->
      <div class="relative w-8 h-8 flex items-center justify-center text-primary-light">
         <svg viewBox="0 0 24 24" fill="none" class="w-8 h-8 text-secondary transform group-hover:scale-110 transition-transform duration-300">
          <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5" stroke="currentColor" stroke-width="2" stroke-linecap="round" stroke-linejoin="round"/>
        </svg>
      </div>
      <span class="text-2xl font-bold font-sans tracking-tight">Grostore</span>
    </a>

    <!-- Desktop Menu -->
    <ul class="hidden lg:flex items-center gap-8 list-none">
      <li v-for="link in navLinks" :key="link.name" class="relative group">
        <a :href="link.href" class="text-sm font-semibold hover:text-secondary transition-colors flex items-center gap-1">
          {{ link.name }}
          <svg v-if="link.hasDropdown" class="w-3 h-3 transition-transform group-hover:rotate-180" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M19 9l-7 7-7-7" />
          </svg>
        </a>
      </li>
    </ul>

    <!-- Actions -->
    <div class="hidden md:flex items-center gap-4">
      <!-- Search -->
      <button class="p-2 hover:bg-white/10 rounded-full transition-colors group">
        <svg class="w-5 h-5 group-hover:text-secondary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
        </svg>
      </button>

      <!-- Cart -->
      <button class="relative p-2 hover:bg-white/10 rounded-full transition-colors group mr-4">
        <svg class="w-5 h-5 group-hover:text-secondary" fill="none" viewBox="0 0 24 24" stroke="currentColor">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
        </svg>
        <span class="absolute top-0 right-0 bg-secondary text-white text-[10px] font-bold w-4 h-4 rounded-full flex items-center justify-center transform group-hover:scale-110 transition-transform">2</span>
      </button>

      <!-- Register Button -->
      <a href="#" class="bg-white text-primary font-bold text-sm py-2.5 px-6 rounded shadow-lg hover:bg-secondary hover:text-white transition-all duration-300 transform hover:-translate-y-0.5">
        Register Now
      </a>
    </div>

    <!-- Mobile Menu Button -->
    <button @click="menuOpen = !menuOpen" class="lg:hidden p-2 text-white">
      <svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
        <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M4 6h16M4 12h16M4 18h16" />
      </svg>
    </button>

    <!-- Mobile Menu Overlay -->
    <div v-if="menuOpen" class="fixed inset-0 bg-primary z-50 flex flex-col items-center justify-center space-y-8 lg:hidden">
      <button @click="menuOpen = false" class="absolute top-6 right-6 text-white p-2">
        <svg class="w-8 h-8" fill="none" stroke="currentColor" viewBox="0 0 24 24">
          <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M6 18L18 6M6 6l12 12" />
        </svg>
      </button>
      
      <a v-for="link in navLinks" :key="link.name" :href="link.href" class="text-2xl font-bold hover:text-secondary transition-colors" @click="menuOpen = false">
        {{ link.name }}
      </a>
      
      <div class="flex gap-6 mt-8">
        <button class="p-3 bg-white/10 rounded-full">
           <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M21 21l-6-6m2-5a7 7 0 11-14 0 7 7 0 0114 0z" />
          </svg>
        </button>
        <button class="relative p-3 bg-white/10 rounded-full">
          <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M16 11V7a4 4 0 00-8 0v4M5 9h14l1 12H4L5 9z" />
          </svg>
           <span class="absolute top-0 right-0 bg-secondary text-white text-xs font-bold w-5 h-5 rounded-full flex items-center justify-center">2</span>
        </button>
      </div>

       <a href="#" class="bg-white text-primary font-bold text-lg py-3 px-10 rounded shadow-lg hover:bg-secondary hover:text-white transition-all">
        Register Now
      </a>
    </div>
  </nav>
</template>
