<template>
  <div class="landing-page">
    <main>
      <LandingHero />
      <PlatformSection />
      <SolutionsSection />
      <IndustriesSection />
      <WhyPeoplePayrollSection />
      <ResourcesSection />
      <ClosingCtaSection />
    </main>
    <LandingFooter />
  </div>
</template>

<script setup>
import LandingHero from './components/landing/LandingHero.vue';
import PlatformSection from './components/landing/PlatformSection.vue';
import SolutionsSection from './components/landing/SolutionsSection.vue';
import IndustriesSection from './components/landing/IndustriesSection.vue';
import WhyPeoplePayrollSection from './components/landing/WhyPeoplePayrollSection.vue';
import ResourcesSection from './components/landing/ResourcesSection.vue';
import ClosingCtaSection from './components/landing/ClosingCtaSection.vue';
import LandingFooter from './components/landing/LandingFooter.vue';
import './components/landing/landing-page.css';
</script>
