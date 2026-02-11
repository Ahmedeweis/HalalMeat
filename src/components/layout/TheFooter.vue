<template>
    <footer class="bg-gray-900 text-white pt-20 pb-10">
        <div class="container mx-auto px-4 md:px-8 lg:px-16">

            <!-- Newsletter -->
            <div
                class="flex flex-col md:flex-row items-center justify-between border-b border-gray-800 pb-12 mb-12 gap-8">
                <div class="text-center md:text-left">
                    <h3 class="text-2xl font-bold mb-2">Subscribe Our Newsletter</h3>
                    <p class="text-gray-400">Get the latest updates and offers directly in your inbox.</p>
                </div>
                <div class="flex w-full md:w-auto max-w-md">
                    <input type="email" placeholder="Your Email Address"
                        class="w-full px-6 py-3 rounded-l-full bg-gray-800 border-none focus:ring-2 focus:ring-secondary outline-none text-white" />
                    <button
                        class="bg-secondary hover:bg-orange-600 text-white font-bold px-8 py-3 rounded-r-full transition-colors whitespace-nowrap">
                        Subscribe
                    </button>
                </div>
            </div>

            <!-- Links Grid -->
            <div class="grid grid-cols-1 md:grid-cols-2 lg:grid-cols-4 gap-12 mb-16">

                <!-- About -->
                <div class="space-y-4">
                    <a href="/" class="flex items-center gap-2 mb-4 group">
                        <svg viewBox="0 0 24 24" fill="none" class="w-8 h-8 text-secondary">
                            <path d="M12 2L2 7l10 5 10-5-10-5zM2 17l10 5 10-5M2 12l10 5 10-5" stroke="currentColor"
                                stroke-width="2" stroke-linecap="round" stroke-linejoin="round" />
                        </svg>
                        <span class="text-2xl font-bold font-sans tracking-tight">Grostore</span>
                    </a>
                    <p class="text-gray-400 text-sm leading-relaxed">
                        Energistically harness progressive technology for top-line catalysts for change. Rapidly
                        monetize one-to-one e-markets.
                    </p>
                    <div class="flex gap-4 pt-2">
                        <a href="#"
                            class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-secondary transition-colors"><span
                                class="sr-only">Facebook</span>f</a>
                        <a href="#"
                            class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-secondary transition-colors"><span
                                class="sr-only">Twitter</span>t</a>
                        <a href="#"
                            class="w-10 h-10 rounded-full bg-gray-800 flex items-center justify-center hover:bg-secondary transition-colors"><span
                                class="sr-only">Instagram</span>i</a>
                    </div>
                </div>

                <!-- Quick Links -->
                <div>
                    <h4 class="font-bold text-lg mb-6">Quick Links</h4>
                    <ul class="space-y-3 text-gray-400 text-sm">
                        <li><a href="#" class="hover:text-secondary transition-colors">My Account</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Order History</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Order Tracking</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Best Seller</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">New Arrivals</a></li>
                    </ul>
                </div>

                <!-- Categories -->
                <div>
                    <h4 class="font-bold text-lg mb-6">Categories</h4>
                    <ul class="space-y-3 text-gray-400 text-sm">
                        <li><a href="#" class="hover:text-secondary transition-colors">Fresh Meat</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Frozen Meat</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Processed Meat</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Organic Meat</a></li>
                        <li><a href="#" class="hover:text-secondary transition-colors">Lean Meat</a></li>
                    </ul>
                </div>

                <!-- Contact -->
                <div>
                    <h4 class="font-bold text-lg mb-6">Contact Us</h4>
                    <ul class="space-y-4 text-gray-400 text-sm">
                        <li class="flex items-start gap-3">
                            <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M17.657 16.657L13.414 20.9a1.998 1.998 0 01-2.827 0l-4.244-4.243a8 8 0 1111.314 0z" />
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M15 11a3 3 0 11-6 0 3 3 0 016 0z" />
                            </svg>
                            123 Street Name, City, United States
                        </li>
                        <li class="flex items-center gap-3">
                            <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M3 8l7.89 5.26a2 2 0 002.22 0L21 8M5 19h14a2 2 0 002-2V7a2 2 0 00-2-2H5a2 2 0 00-2 2v10a2 2 0 002 2z" />
                            </svg>
                            support@grostore.com
                        </li>
                        <li class="flex items-center gap-3">
                            <svg class="w-5 h-5 text-secondary flex-shrink-0" fill="none" viewBox="0 0 24 24"
                                stroke="currentColor">
                                <path stroke-linecap="round" stroke-linejoin="round" stroke-width="2"
                                    d="M3 5a2 2 0 012-2h3.28a1 1 0 01.948.684l1.498 4.493a1 1 0 01-.502 1.21l-2.257 1.13a11.042 11.042 0 005.516 5.516l1.13-2.257a1 1 0 011.21-.502l4.493 1.498a1 1 0 01.684.949V19a2 2 0 01-2 2h-1C9.716 21 3 14.284 3 6V5z" />
                            </svg>
                            +1 234 567 890
                        </li>
                    </ul>
                </div>

            </div>

            <!-- Copyright -->
            <div
                class="border-t border-gray-800 pt-8 flex flex-col md:flex-row items-center justify-between text-sm text-gray-500">
                <p>&copy; 2026 Grostore. All Rights Reserved.</p>
                <div class="flex gap-4 mt-4 md:mt-0">
                    <a href="#" class="hover:text-white transition-colors">Privacy Policy</a>
                    <a href="#" class="hover:text-white transition-colors">Terms & Conditions</a>
                </div>
            </div>

        </div>
    </footer>
</template>
