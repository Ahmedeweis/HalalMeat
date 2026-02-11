<script setup>
const features = [
    { id: 1, title: '100% Payment Secure', text: 'We ensure secure payment with top-tier encryption.', icon: 'lock' },
    { id: 2, title: '100% Fresh & Organic', text: 'Quality products directly from farm to table.', icon: 'leaf' },
    { id: 3, title: 'Delivery Executively', text: 'Professional delivery right to your doorstep.', icon: 'truck' },
    { id: 4, title: 'Environmentally Products', text: 'Sustainable packaging for a greener planet.', icon: 'recycle' },
    { id: 5, title: 'Pure Fresh Meat', text: 'Hand-picked premium cuts of halal meat.', icon: 'check-circle' },
    { id: 6, title: '100% Return Secure', text: 'Easy returns if you are not satisfied.', icon: 'rotate-cw' },
]
</script>

<template>
    <section class="py-20 overflow-hidden relative">
        <div class="container mx-auto px-4 md:px-8 lg:px-16 text-center">

            <!-- Section Header -->
            <div class="mb-16">
                <span class="text-secondary text-xs font-bold uppercase tracking-wider mb-2 block">Why Choose Us</span>
                <h2 class="text-3xl md:text-4xl font-bold text-primary dark:text-white">Why Us Choose Grostore Halal
                    Products</h2>
            </div>

            <!-- Content Wrapper -->
            <div class="relative flex flex-col lg:flex-row items-center justify-center gap-12 lg:gap-0">

                <!-- Left Features -->
                <div class="flex flex-col gap-10 lg:w-1/3 lg:items-end lg:text-right">
                    <div v-for="feature in features.slice(0, 3)" :key="feature.id"
                        class="flex flex-col lg:flex-row items-center gap-4 group">
                        <div
                            class="w-12 h-12 rounded-full bg-white shadow-lg flex items-center justify-center text-secondary group-hover:bg-secondary group-hover:text-white transition-colors duration-300">
                            <!-- Icon Placeholder -->
                            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M5 13l4 4L19 7" />
                            </svg>
                        </div>
                        <div>
                            <h4 class="font-bold text-gray-900 dark:text-white">{{ feature.title }}</h4>
                            <p class="text-sm text-gray-500 max-w-xs">{{ feature.text }}</p>
                        </div>
                    </div>
                </div>

                <!-- Center Image -->
                <div class="relative lg:w-1/3 flex justify-center">
                    <div class="relative w-80 h-80 lg:w-96 lg:h-96">
                        <!-- Animated Rings -->
                        <div
                            class="absolute inset-0 border-2 border-dashed border-primary/20 rounded-full animate-spin-slow">
                        </div>
                        <div class="absolute inset-4 border border-primary/10 rounded-full"></div>

                        <!-- Main Image Mask -->
                        <div
                            class="absolute inset-0 rounded-full overflow-hidden border-8 border-white shadow-2xl z-10">
                            <img src="https://placehold.co/400x400/1e293b/FFFFFF?text=Butcher" alt="Happy Butcher"
                                class="w-full h-full object-cover" />
                        </div>

                        <!-- Play Button Overlay -->
                        <button
                            class="absolute top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2 w-16 h-16 bg-secondary text-white rounded-full flex items-center justify-center shadow-lg hover:scale-110 transition-transform z-20 animate-pulse">
                            <svg class="w-8 h-8 ml-1" fill="currentColor" viewBox="0 0 20 20">
                                <path
                                    d="M6.3 2.841A1.5 1.5 0 004 4.11V15.89a1.5 1.5 0 002.3 1.269l9.344-5.89a1.5 1.5 0 000-2.538L6.3 2.84z" />
                            </svg>
                        </button>
                    </div>
                </div>

                <!-- Right Features -->
                <div class="flex flex-col gap-10 lg:w-1/3 lg:items-start lg:text-left">
                    <div v-for="feature in features.slice(3, 6)" :key="feature.id"
                        class="flex flex-col lg:flex-row-reverse items-center gap-4 group">
                        <div
                            class="w-12 h-12 rounded-full bg-white shadow-lg flex items-center justify-center text-secondary group-hover:bg-secondary group-hover:text-white transition-colors duration-300">
                            <svg class="w-6 h-6" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M5 13l4 4L19 7" />
                            </svg>
                        </div>
                        <div>
                            <h4 class="font-bold text-gray-900 dark:text-white">{{ feature.title }}</h4>
                            <p class="text-sm text-gray-500 max-w-xs">{{ feature.text }}</p>
                        </div>
                    </div>
                </div>

            </div>

        </div>
    </section>
</template>
