<template>
  <section id="resources" class="resources-section">
    <div class="resources-heading">
      <div>
        <span class="section-kicker">A GOOD PLACE TO START</span>
        <h2>Useful next steps for your people.</h2>
      </div>
      <p>Explore the platform, learn about open roles, or head straight to your account.</p>
    </div>
    <div class="resource-grid">
      <article class="resource-card resource-card--orange">
        <span>FOR PEOPLE TEAMS</span>
        <h3>Bring your HR work into one view.</h3>
        <p>See how people records, payroll, time, and hiring connect across the platform.</p>
        <QBtn flat no-caps label="Explore solutions" icon-right="arrow_forward" href="#solutions" />
      </article>
      <article class="resource-card">
        <span>FOR CANDIDATES</span>
        <h3>Find your next opportunity.</h3>
        <p>Browse current vacancies and learn more about joining a team.</p>
        <QBtn flat no-caps label="View open roles" icon-right="arrow_forward" href="/careers" />
      </article>
      <article class="resource-card resource-card--navy">
        <span>FOR YOUR TEAM</span>
        <h3>Pick up where you left off.</h3>
        <p>Sign in to manage your work, people, and payroll tasks.</p>
        <QBtn flat no-caps label="Go to sign in" icon-right="arrow_forward" href="/login" />
      </article>
    </div>
  </section>
</template>

<script setup>
import { QBtn } from 'quasar';
</script>
