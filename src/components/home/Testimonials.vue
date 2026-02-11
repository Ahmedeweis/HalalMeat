<script setup>
const testimonials = [
    { id: 1, name: 'Best Online Halal Shop', author: 'Amir Khan', text: 'Improvents rather than covalent methodologies. Completely negotiate accurate networks with clicks-and-mortar innovation.', rating: 5 },
    { id: 2, name: 'Superb Quality', author: 'Saiful Talukdar', text: 'Improvents rather than covalent methodologies. Completely negotiate accurate networks with clicks-and-mortar innovation.', rating: 5 },
    { id: 3, name: 'Best Service', author: 'Fernando A. Hule', text: 'Improvents rather than covalent methodologies. Completely negotiate accurate networks with clicks-and-mortar innovation.', rating: 5 },
]
</script>

<template>
    <section class="py-20 bg-gray-50 dark:bg-bg/50">
        <div class="container mx-auto px-4 md:px-8 lg:px-16 text-center">

            <div class="mb-12">
                <span class="text-secondary text-xs font-bold uppercase tracking-wider mb-2 block">Customer
                    Feedback</span>
                <h2 class="text-3xl md:text-4xl font-bold text-primary dark:text-white">Our Satisfied Customer Feedback
                </h2>
            </div>

            <div class="grid grid-cols-1 md:grid-cols-3 gap-8">
                <div v-for="testimonial in testimonials" :key="testimonial.id"
                    class="bg-white dark:bg-card p-8 rounded-2xl shadow-lg relative text-left hover:-translate-y-2 transition-transform duration-300">
                    <!-- Quote Icon -->
                    <div
                        class="absolute -top-4 right-8 w-12 h-12 bg-secondary text-white rounded-full flex items-center justify-center text-2xl font-serif">
                        "
                    </div>

                    <h4 class="font-bold text-lg mb-2 text-gray-900 dark:text-white">{{ testimonial.name }}</h4>
                    <p class="text-gray-500 text-sm mb-6 leading-relaxed">{{ testimonial.text }}</p>

                    <div class="flex items-center justify-between mt-auto">
                        <div class="font-bold text-primary text-sm">{{ testimonial.author }}</div>
                        <div class="flex text-yellow-400 text-xs">
                            <span v-for="i in testimonial.rating" :key="i">★</span>
                        </div>
                    </div>
                </div>
            </div>

        </div>
    </section>
</template>
