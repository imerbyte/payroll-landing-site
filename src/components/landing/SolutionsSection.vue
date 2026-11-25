<template>
  <section id="solutions" class="features">
    <div class="features-heading">
      <div>
        <span>HR THAT MOVES WITH YOUR TEAM</span>
        <h2>Support every part of the employee journey.</h2>
      </div>
      <p>Give every team member a simpler way to manage the moments that shape their work.</p>
    </div>

    <div class="feature-grid">
      <article class="feature-card feature-card--featured">
        <span class="feature-number">01</span>
        <div class="feature-icon"><QIcon name="payments" /></div>
        <h3>Confident payroll</h3>
        <p>Process earnings, deductions, taxes, and reports with fewer manual steps.</p>
        <QBtn flat no-caps label="Explore payroll" icon-right="arrow_forward" href="#platform" />
      </article>
      <article class="feature-card">
        <span class="feature-number">02</span>
        <div class="feature-icon"><QIcon name="badge" /></div>
        <h3>Complete employee records</h3>
        <p>Keep profiles, documents, contracts, and employment history together.</p>
      </article>
      <article class="feature-card">
        <span class="feature-number">03</span>
        <div class="feature-icon"><QIcon name="event_available" /></div>
        <h3>Time and leave</h3>
        <p>Coordinate attendance, requests, approvals, schedules, and availability.</p>
      </article>
      <article class="feature-card">
        <span class="feature-number">04</span>
        <div class="feature-icon"><QIcon name="how_to_reg" /></div>
        <h3>Hiring without friction</h3>
        <p>Publish vacancies and move candidates through a clear recruitment flow.</p>
      </article>
      <article class="feature-card">
        <span class="feature-number">05</span>
        <div class="feature-icon"><QIcon name="trending_up" /></div>
        <h3>Growth and performance</h3>
        <p>Bring goals, reviews, and employee development into the people conversation.</p>
      </article>
    </div>
  </section>
</template>

<script setup>
import { QBtn, QIcon } from 'quasar';
</script>
