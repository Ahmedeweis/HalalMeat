<template>
    <section class="py-16 bg-gray-50 dark:bg-bg/50">
        <div class="container mx-auto px-4 md:px-8 lg:px-16">

            <div class="grid grid-cols-1 md:grid-cols-2 gap-8">

                <!-- Banner 1: Fresh Meat -->
                <div
                    class="relative bg-primary-dark rounded-3xl overflow-hidden p-8 md:p-12 flex flex-col justify-center min-h-[300px] shadow-2xl group">
                    <!-- Background pattern/gradient -->
                    <div
                        class="absolute inset-0 bg-gradient-to-r from-primary-dark via-primary to-transparent opacity-90 z-10">
                    </div>
                    <div
                        class="absolute right-0 top-0 h-full w-2/3 bg-[url('https://placehold.co/600x400/1e293b/FFFFFF?text=Fresh+Meat')] bg-cover bg-center transition-transform duration-700 group-hover:scale-110">
                    </div>

                    <!-- Content -->
                    <div class="relative z-20 max-w-xs space-y-4">
                        <span
                            class="text-red-500 font-bold bg-white/10 px-3 py-1 rounded backdrop-blur-sm text-xs uppercase tracking-wider block w-fit">Limited
                            Time Offer</span>
                        <h3 class="text-3xl md:text-4xl font-bold text-white leading-tight">
                            Fresh Meat <br>
                            Best For Your Family
                        </h3>
                        <button
                            class="bg-secondary hover:bg-white hover:text-secondary text-white font-bold py-3 px-8 rounded shadow-lg transition-colors flex items-center gap-2 mt-4 w-fit">
                            Shop Now
                            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M17 8l4 4m0 0l-4 4m4-4H3" />
                            </svg>
                        </button>
                    </div>

                    <!-- Decorative Badge -->
                    <div
                        class="absolute bottom-6 left-1/2 md:left-auto md:right-10 transform -translate-x-1/2 md:translate-x-0 w-24 h-24 bg-green-500 rounded-full flex flex-col items-center justify-center text-white font-bold z-20 shadow-lg animate-bounce">
                        <span class="text-xs uppercase">Discount</span>
                        <span class="text-3xl leading-none">50%</span>
                    </div>
                </div>

                <!-- Banner 2: Smoothie -->
                <div
                    class="relative bg-pink-100 dark:bg-pink-900/20 rounded-3xl overflow-hidden p-8 md:p-12 flex flex-col justify-center min-h-[300px] shadow-xl group">
                    <!-- Background Image -->
                    <div
                        class="absolute right-0 bottom-0 h-full w-1/2 bg-[url('https://placehold.co/400x400/fbcfe8/be185d?text=Smoothie')] bg-contain bg-no-repeat bg-right-bottom transition-transform duration-500 group-hover:scale-105">
                    </div>

                    <!-- Content -->
                    <div class="relative z-20 max-w-xs space-y-4">
                        <span class="text-pink-600 font-bold text-xs uppercase tracking-wider block">Best Selling</span>
                        <h3 class="text-3xl md:text-4xl font-bold text-gray-900 dark:text-white leading-tight">
                            Best Smoothie
                        </h3>
                        <p class="text-gray-500 text-sm">Deliciously refreshing organic fruit blends.</p>

                        <button
                            class="bg-pink-500 hover:bg-pink-600 text-white font-bold py-3 px-8 rounded shadow-lg transition-colors flex items-center gap-2 mt-4 w-fit">
                            Shop Now
                            <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M17 8l4 4m0 0l-4 4m4-4H3" />
                            </svg>
                        </button>
                    </div>
                </div>

            </div>
        </div>
    </section>
</template>
