<template>
  <section class="py-20 bg-gray-50 dark:bg-bg/50">
    <div class="container mx-auto px-4 md:px-8 lg:px-16 flex flex-col lg:flex-row items-center gap-12 lg:gap-20">
      
      <!-- Text Content (Left) -->
      <div class="lg:w-1/2 space-y-6">
        <span class="inline-block px-4 py-1.5 rounded-full bg-orange-100 text-secondary font-bold text-xs uppercase tracking-wider">
          We Provide Halal Products
        </span>
        <h2 class="text-4xl md:text-5xl font-bold text-primary dark:text-white leading-tight">
          Make the World Better <br>
          <span class="text-secondary">Halal Products.</span>
        </h2>
        <p class="text-gray-500 text-lg">
          Energistically harness progressive technology for top-line catalysts for change. Rapidly monetize one-to-one e-markets for high standards.
        </p>
        <p class="text-gray-500">
          Objectively actualize e-business e-tailers rather than market positioning intellectual capital. Dynamically create cross-unit testing procedures and corporate markets.
        </p>
        
        <button class="bg-secondary hover:bg-orange-600 text-white font-bold py-3 px-8 rounded shadow-lg transition-transform transform hover:-translate-y-1 flex items-center gap-2 mt-4">
          Learn More
          <svg class="w-5 h-5" fill="none" viewBox="0 0 24 24" stroke="currentColor">
            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M17 8l4 4m0 0l-4 4m4-4H3" />
          </svg>
        </button>

        <!-- Floating Chicken Icon (Decorative) -->
        <div class="absolute -bottom-10 left-0 w-24 h-24 opacity-20 pointer-events-none">
           <!-- SVG or Image -->
        </div>
      </div>

      <!-- Image Grid (Right) -->
      <div class="lg:w-1/2 relative">
        <div class="grid grid-cols-2 gap-4">
          <!-- Chef Image -->
          <div class="col-span-1 row-span-2 relative rounded-2xl overflow-hidden shadow-2xl transform translate-y-12">
            <img src="https://placehold.co/400x600/1e293b/FFFFFF?text=Chef" alt="Our Chef" class="w-full h-full object-cover rounded-2xl transform hover:scale-105 transition-transform duration-500" />
            
            <!-- Badge -->
            <div class="absolute top-4 right-4 bg-white p-2 rounded-full shadow-lg animate-spin-slow">
              <svg class="w-12 h-12 text-primary" viewBox="0 0 24 24" fill="currentColor">
                <!-- Simple Halal Badge SVG -->
                <circle cx="12" cy="12" r="10" stroke="currentColor" stroke-width="2" fill="none"/>
                <path d="M12 7v5l3 3" stroke="currentColor" stroke-width="2" stroke-linecap="round"/>
              </svg>
            </div>
          </div>

          <!-- Delivery Guy / Dish Image -->
          <div class="col-span-1 rounded-2xl overflow-hidden shadow-xl transform -translate-y-4">
            <img src="https://placehold.co/400x300/1e293b/FFFFFF?text=Delivery" alt="Fresh Delivery" class="w-full h-full object-cover rounded-2xl transform hover:scale-105 transition-transform duration-500" />
          </div>

           <!-- Another Image or Decorative Block -->
           <div class="col-span-1 rounded-2xl overflow-hidden shadow-xl transform translate-y-4 bg-secondary/10 flex items-center justify-center p-4">
              <div class="text-center">
                 <h4 class="font-bold text-primary text-xl">100%</h4>
                 <p class="text-sm text-gray-600">Organic</p>
              </div>
          </div>
        </div>

        <!-- Decorative Elements -->
        <div class="absolute -z-10 top-1/2 right-0 w-64 h-64 bg-primary/5 rounded-full blur-3xl"></div>
      </div>

    </div>
  </section>
</template>
