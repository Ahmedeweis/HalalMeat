<template>
  <section class="relative bg-primary overflow-hidden min-h-screen flex flex-col pt-20">
    <!-- Background Decor -->
    <div class="absolute inset-0 opacity-10 pointer-events-none">
       <!-- Subtle Pattern (Hexagons or similar) -->
       <svg width="100%" height="100%" xmlns="http://www.w3.org/2000/svg">
         <defs>
           <pattern id="hexagons" width="50" height="43.4" patternUnits="userSpaceOnUse" patternTransform="scale(2)">
             <path d="M25 0L50 14.4v28.8L25 57.7L0 43.2V14.4z" fill="none" stroke="currentColor" stroke-width="1"/>
           </pattern>
         </defs>
         <rect width="100%" height="100%" fill="url(#hexagons)" class="text-white"/>
       </svg>
    </div>
    
    <!-- Gradient Overlay -->
    <div class="absolute inset-0 bg-gradient-to-br from-primary-light/20 via-primary to-primary-dark/80"></div>

    <!-- Content Container -->
    <div class="relative container mx-auto px-4 md:px-8 lg:px-16 flex-grow flex items-center">
      <div class="grid grid-cols-1 lg:grid-cols-2 gap-12 w-full py-12 lg:py-0">
        <slot />
      </div>
    </div>

    <!-- Bottom Feature Bar Slot -->
    <div class="relative z-20 mt-auto">
      <slot name="footer" />
    </div>
  </section>
</template>
