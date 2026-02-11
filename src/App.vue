<script setup>
import NavBar from './components/layout/NavBar.vue'
import HeroWrapper from './components/hero/HeroWrapper.vue'
import HeroText from './components/hero/HeroText.vue'
import HeroVisuals from './components/hero/HeroVisuals.vue'
import FeatureBar from './components/hero/FeatureBar.vue'
import CategorySection from './components/home/CategorySection.vue'
import MissionSection from './components/home/MissionSection.vue'
import ProductSection from './components/home/ProductSection.vue'
import PromoSection from './components/home/PromoSection.vue'
import WhyChooseUs from './components/home/WhyChooseUs.vue'
import Testimonials from './components/home/Testimonials.vue'
import TheFooter from './components/layout/TheFooter.vue'
</script>

<template>
  <div
    class="font-sans antialiased text-gray-900 bg-white dark:bg-bg min-h-screen selection:bg-secondary selection:text-white">
    <!-- Header -->
    <NavBar />

    <!-- Hero Section -->
    <HeroWrapper>
      <!-- Left Content -->
      <HeroText badgeText="Best Quality Halal Products" title="Halal Meat & Grocery Delivery Service In America"
        subtitle="Energistically harness progressive technology for top-line catalysts for change." />

      <!-- Right Visuals -->
      <HeroVisuals />

      <!-- Footer Features -->
      <template #footer>
        <FeatureBar />
      </template>
    </HeroWrapper>

    <!-- Categories Section -->
    <CategorySection />

    <!-- Best Sellers Section -->
    <ProductSection title="Shop Best Sellers" />

    <!-- Mission Section -->
    <MissionSection />

    <!-- Promo Banners -->
    <PromoSection />

    <!-- Why Choose Us -->
    <WhyChooseUs />

    <!-- Frozen Foods Collection (Reusing ProductSection with different title and categories) -->
    <ProductSection title="Grostore Halal Frozen Foods Collection"
      :categories="['Meal Kits', 'Halal Chicken', 'Goat Meat', 'Ship Meat', 'Halal Deli']"
      class="bg-orange-50/50 dark:bg-bg/50" />

    <!-- Testimonials -->
    <Testimonials />

    <!-- Footer -->
    <TheFooter />
  </div>
</template>

<style>
/* Global Styles could go here or in index.css */
</style>
