<template>
  <div class="public-layout">
    <header class="public-header">
      <div class="public-toolbar">
        <a class="brand-button" href="/" aria-label="People and Payroll home">
          <img src="/belize-coat-of-arms.png" class="brand-mark" alt="" />
          <span>People &amp; Payroll</span>
        </a>
        <nav class="public-nav" aria-label="Primary navigation">
          <a href="#platform">Platform</a>
          <a href="#solutions">Solutions</a>
          <a href="#industries">Industries</a>
          <a href="#resources">Resources</a>
        </nav>
        <a class="public-sign-in" href="/login">Sign in</a>
      </div>
    </header>
    <LandingPage />
  </div>
</template>

<script setup>
import LandingPage from './LandingPage.vue';
</script>
