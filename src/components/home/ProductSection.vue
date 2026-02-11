<script setup>
import { ref } from 'vue'
import ProductCard from './ProductCard.vue'

const props = defineProps({
    title: String,
    categories: {
        type: Array,
        default: () => ['All', 'Beef Meat', 'Halal Chicken', 'Goat Meat', 'Ship Meat', 'Halal Deli']
    }
})

const activeTab = ref(props.categories[0])

// Mock Products - In real app, props.products or fetch based on activeTab
const products = [
    { id: 1, name: 'Halal Sliced Beef Pepperoni Pizzas & Calzones', price: 88.00, oldPrice: 96.00, discount: 50, rating: 5, reviews: 3, image: 'https://placehold.co/300x300?text=Beef+Pizza' },
    { id: 2, name: 'Fresh Halal Beef Steaks 1kg', price: 55.00, oldPrice: 65.00, discount: 20, rating: 4, reviews: 12, image: 'https://placehold.co/300x300?text=Beef+Steak' },
    { id: 3, name: 'Premium Goat Meat Cuts', price: 95.00, oldPrice: 110.00, discount: 15, rating: 5, reviews: 8, image: 'https://placehold.co/300x300?text=Goat+Meat' },
    { id: 4, name: 'Halal Chicken Breast Fillets', price: 35.00, oldPrice: 40.00, discount: 10, rating: 4, reviews: 25, image: 'https://placehold.co/300x300?text=Chicken' },
]
</script>

<template>
    <section class="py-16">
        <div class="container mx-auto px-4 md:px-8 lg:px-16">

            <!-- Header with Tabs -->
            <div class="flex flex-col md:flex-row items-center justify-between mb-10 gap-6">
                <div class="text-center md:text-left">
                    <span class="text-secondary text-xs font-bold uppercase tracking-wider mb-2 block">Best For
                        You</span>
                    <h2 class="text-3xl font-bold text-primary dark:text-white">{{ title || 'Shop Best Sellers' }}</h2>
                </div>

                <!-- Filter Tabs -->
                <div class="flex flex-wrap justify-center gap-4">
                    <button v-for="cat in categories" :key="cat" @click="activeTab = cat"
                        class="text-sm font-semibold transition-colors relative"
                        :class="activeTab === cat ? 'text-secondary font-bold' : 'text-gray-500 hover:text-primary'">
                        {{ cat }}
                        <span v-if="activeTab === cat"
                            class="absolute -bottom-2 left-0 w-full h-0.5 bg-secondary"></span>
                    </button>
                </div>

                <!-- Arrows (Optional) -->
                <div class="hidden md:flex gap-2">
                    <button
                        class="w-8 h-8 rounded-full border border-gray-200 text-gray-400 hover:bg-primary hover:text-white flex items-center justify-center transition-colors">
                        <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M15 19l-7-7 7-7" />
                        </svg>
                    </button>
                    <button
                        class="w-8 h-8 rounded-full bg-secondary text-white flex items-center justify-center hover:bg-orange-600 transition-colors">
                        <svg class="w-4 h-4" fill="none" viewBox="0 0 24 24" stroke="currentColor">
                            <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2" d="M9 5l7 7-7 7" />
                        </svg>
                    </button>
                </div>
            </div>

            <!-- Products Grid -->
            <div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-6">
                <ProductCard v-for="product in products" :key="product.id" :product="product" />
            </div>

        </div>
    </section>
</template>
