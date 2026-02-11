<template>
  <div class="relative flex items-center justify-center h-full min-h-[400px] lg:min-h-[600px]">
    <!-- Background Blob/Splash -->
    <div class="absolute inset-0 bg-secondary/5 blur-[100px] rounded-full transform scale-75 animate-pulse"></div>

    <!-- Main Dish Image (Placeholder for now) -->
    <div class="relative w-[300px] h-[300px] md:w-[450px] md:h-[450px] rounded-full shadow-2xl overflow-hidden border-4 border-white/10 z-10 animate-float-slow">
       <img src="/hero-dish.svg" alt="Halal Meat Platter" class="w-full h-full object-cover" />
    </div>

    <!-- Floating Elements -->
    
    <!-- Halal Badge (Top Right) -->
    <div class="absolute top-10 right-0 md:right-10 w-24 h-24 md:w-32 md:h-32 bg-white rounded-full shadow-xl flex items-center justify-center z-20 animate-spin-slow">
      <!-- Halal Text Circular -->
      <svg viewBox="0 0 100 100" class="w-full h-full p-2">
        <path id="curve" d="M 50, 50 m -37, 0 a 37,37 0 1,1 74,0 a 37,37 0 1,1 -74,0" fill="transparent"/>
        <text width="100">
          <textPath xlink:href="#curve" class="text-[11px] font-bold uppercase tracking-widest fill-primary">
            • Halal Certified • Halal Certified
          </textPath>
        </text>
        <!-- Center Icon -->
        <text x="50" y="55" text-anchor="middle" class="text-3xl fill-secondary font-bold">حلال</text>
      </svg>
    </div>

    <!-- Chili Pepper (Bottom Left) -->
    <div class="absolute bottom-20 left-0 md:left-10 w-16 h-16 z-20 animate-bounce delay-700">
       <svg viewBox="0 0 24 24" fill="none" class="w-full h-full text-red-600 drop-shadow-lg transform -rotate-45">
         <path d="M12.986 6.366C15.658 3.694 18.006 2 21 2c.5 3 0 6-3 9l-7.5 7.5a4.95 4.95 0 01-7-7l7.5-7.5c.667-.667 1.328-1.328 1.986-1.986z" fill="currentColor"/>
         <path d="M16 5l3 3" stroke="#991B1B" stroke-width="2" stroke-linecap="round"/>
       </svg>
    </div>

    <!-- Leaf (Top Left) -->
    <div class="absolute top-20 left-0 w-12 h-12 z-20 animate-float-slow delay-1000">
       <svg viewBox="0 0 24 24" fill="none" class="w-full h-full text-green-500 drop-shadow-lg transform rotate-12">
          <path d="M2.00003 12C2.00003 12 4.00003 6.00003 10 4.00003C11.171 7.68303 9.48203 11 9.48203 11C9.48203 11 15 10 18 13C18 13 22 21 13 22C4.00003 23 2.00003 12 2.00003 12Z" fill="currentColor"/>
       </svg>
    </div>

     <!-- Leaf (Bottom Right) -->
    <div class="absolute bottom-10 right-10 w-10 h-10 z-10 animate-float-slow delay-500">
       <svg viewBox="0 0 24 24" fill="none" class="w-full h-full text-green-400 drop-shadow-lg transform -rotate-12 blur-[1px]">
          <path d="M22 12C22 12 20 18 14 20C12.829 16.317 14.518 13 14.518 13C14.518 13 9 14 6 11C6 11 2 3 11 2C20 1 22 12 22 12Z" fill="currentColor"/>
       </svg>
    </div>

  </div>
</template>

<style scoped>
/* Ensure clip path or mask for image works well */
</style>
