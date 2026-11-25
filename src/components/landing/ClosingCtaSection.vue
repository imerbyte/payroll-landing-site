<template>
  <section class="closing-cta">
    <div class="closing-cta__pattern" />
    <div>
      <span>MAKE WORK BETTER FOR EVERYONE</span>
      <h2>Bring your people operations together.</h2>
      <p>Take the next step toward a more connected workday.</p>
    </div>
    <div class="closing-cta__actions">
      <QBtn
        unelevated
        no-caps
        href="/login"
        label="Sign in to get started"
        icon-right="arrow_forward"
        class="closing-primary"
      />
      <QBtn outline no-caps href="/careers" label="Explore careers" class="closing-secondary" />
    </div>
  </section>
</template>

<script setup>
import { QBtn } from 'quasar';
</script>
