<template>
  <section id="platform" class="platform-section">
    <div class="platform-copy">
      <span class="section-kicker">ONE CONNECTED PLATFORM</span>
      <h2>Work flows better when everything works together.</h2>
      <p>
        Replace scattered spreadsheets and disconnected processes with one shared view of your
        people, payroll, and day-to-day work.
      </p>
      <div class="platform-list">
        <div v-for="item in platformItems" :key="item.title" class="platform-list-item">
          <span class="platform-list-icon"><QIcon :name="item.icon" /></span>
          <div><strong>{{ item.title }}</strong><small>{{ item.detail }}</small></div>
        </div>
      </div>
    </div>
    <div class="platform-art">
      <div class="platform-art__glow" />
      <div class="people-card">
        <div class="people-card__header">
          <div><small>PEOPLE DIRECTORY</small><strong>Your team, at a glance</strong></div>
          <QIcon name="more_horiz" />
        </div>
        <div v-for="person in teamPreview" :key="person.name" class="people-row">
          <span class="people-avatar" :class="person.color">{{ person.initials }}</span>
          <div><strong>{{ person.name }}</strong><small>{{ person.role }}</small></div>
          <span class="people-status" :class="person.statusClass">{{ person.status }}</span>
        </div>
        <div class="people-card__footer">
          <QIcon name="lock" />
          Private employee information, in one secure place
        </div>
      </div>
      <div class="payroll-chip"><QIcon name="task_alt" /> Payroll and people data in sync</div>
    </div>
  </section>
</template>

<script setup>
import { QIcon } from 'quasar';
import { platformItems, teamPreview } from './landingContent.js';
</script>
