<template>
  <section id="industries" class="industries-section">
    <div class="industries-heading">
      <span class="section-kicker">MADE FOR THE WAY YOU WORK</span>
      <h2>One platform. Different kinds of teams.</h2>
      <p>Flexible people operations for organizations at every stage and across every sector.</p>
    </div>
    <div class="industry-grid">
      <article v-for="industry in industries" :key="industry.title" class="industry-card">
        <span class="industry-icon"><QIcon :name="industry.icon" /></span>
        <h3>{{ industry.title }}</h3>
        <p>{{ industry.detail }}</p>
      </article>
    </div>
  </section>
</template>

<script setup>
import { QIcon } from 'quasar';
import { industries } from './landingContent.js';
</script>
