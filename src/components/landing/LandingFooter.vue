<template>
  <footer class="site-footer">
    <QBtn flat no-caps href="/" class="footer-brand">
      <img src="/belize-coat-of-arms.png" alt="" />
      <span>People &amp; Payroll</span>
    </QBtn>
    <span class="footer-note">Built for better work in Belize.</span>
    <nav aria-label="Footer navigation">
      <QBtn flat no-caps href="/careers" label="Careers" />
      <QBtn flat no-caps href="/login" label="Sign in" />
    </nav>
    <small>© {{ currentYear }} People &amp; Payroll</small>
  </footer>
</template>

<script setup>
import { QBtn } from 'quasar';

const currentYear = new Date().getFullYear();
</script>
