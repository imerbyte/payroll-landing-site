<template>
  <section class="hero">
    <div class="hero-orb hero-orb--one" />
    <div class="hero-orb hero-orb--two" />

    <div class="hero-inner">
      <div class="hero-copy">
        <div class="eyebrow">
          <span class="eyebrow-mark"><QIcon name="verified" /></span>
          Built for Belizean organizations
        </div>
        <h1>Put people at the <span>heart of work.</span></h1>
        <p>
          Payroll, employee records, leave, recruitment, and performance in one beautifully
          connected platform.
        </p>
        <div class="hero-actions">
          <QBtn
            unelevated
            no-caps
            href="/login"
            label="Sign in to People & Payroll"
            icon-right="arrow_forward"
            class="primary-cta"
          />
          <QBtn outline no-caps href="/careers" label="View open roles" class="secondary-cta" />
        </div>
        <div class="proof-row">
          <div><strong>One</strong><span>secure system</span></div>
          <div><strong>Local</strong><span>Belize ready</span></div>
          <div><strong>Simple</strong><span>daily workflows</span></div>
        </div>
      </div>

      <div class="product-stage" aria-label="People and Payroll dashboard preview">
        <div class="stage-spark stage-spark--one" />
        <div class="stage-spark stage-spark--two" />

        <div class="floating-card floating-card--leave">
          <span class="floating-icon"><QIcon name="event_available" /></span>
          <div><strong>Leave approved</strong><small>Alisha Morgan</small></div>
        </div>

        <div class="product-window">
          <div class="window-header">
            <div class="window-brand">
              <span><QIcon name="groups" /></span>
              People &amp; Payroll
            </div>
            <div class="window-actions">
              <QIcon name="notifications_none" />
              <span>JM</span>
            </div>
          </div>

          <div class="window-layout">
            <aside>
              <div class="nav-active"><QIcon name="grid_view" /><span>Overview</span></div>
              <div><QIcon name="badge" /><span>People</span></div>
              <div><QIcon name="payments" /><span>Payroll</span></div>
              <div><QIcon name="event_available" /><span>Leave</span></div>
              <div><QIcon name="insights" /><span>Reports</span></div>
            </aside>

            <div class="dashboard-main">
              <div class="dashboard-title">
                <div>
                  <small>Monday, 23 November</small>
                  <h2>Good morning, Jamie</h2>
                </div>
                <button type="button">Run payroll <QIcon name="arrow_forward" /></button>
              </div>

              <div class="metric-grid">
                <article>
                  <span class="metric-icon metric-icon--blue"><QIcon name="groups" /></span>
                  <small>Employees</small>
                  <strong>248</strong>
                  <em>+12 this year</em>
                </article>
                <article>
                  <span class="metric-icon metric-icon--orange"><QIcon name="account_balance_wallet" /></span>
                  <small>Next payroll</small>
                  <strong>$86.2k</strong>
                  <em>Due in 4 days</em>
                </article>
                <article>
                  <span class="metric-icon metric-icon--green"><QIcon name="event_busy" /></span>
                  <small>On leave</small>
                  <strong>16</strong>
                  <em>5 pending</em>
                </article>
              </div>

              <div class="dashboard-grid">
                <article class="chart-panel">
                  <div class="panel-heading">
                    <div><small>Payroll cost</small><strong>$86,240</strong></div>
                    <span>6 months</span>
                  </div>
                  <div class="chart">
                    <svg viewBox="0 0 500 160" role="img" aria-label="Payroll cost trend">
                      <defs>
                        <linearGradient id="payrollArea" x1="0" y1="0" x2="0" y2="1">
                          <stop offset="0%" stop-color="var(--q-primary)" stop-opacity=".30" />
                          <stop offset="100%" stop-color="var(--q-primary)" stop-opacity="0" />
                        </linearGradient>
                      </defs>
                      <path class="chart-area" d="M0 128 C50 118 80 96 120 104 S195 76 242 88 S320 43 365 58 S445 24 500 38 L500 160 L0 160 Z" />
                      <path class="chart-line" d="M0 128 C50 118 80 96 120 104 S195 76 242 88 S320 43 365 58 S445 24 500 38" />
                    </svg>
                  </div>
                </article>

                <article class="activity-panel">
                  <div class="panel-heading"><strong>Team activity</strong><span>Today</span></div>
                  <div class="activity-row">
                    <span class="avatar avatar--peach">AL</span>
                    <div><strong>Annual leave</strong><small>Approved</small></div>
                  </div>
                  <div class="activity-row">
                    <span class="avatar avatar--gold">DR</span>
                    <div><strong>Payroll review</strong><small>In progress</small></div>
                  </div>
                  <div class="activity-row">
                    <span class="avatar avatar--green">MS</span>
                    <div><strong>Document added</strong><small>Just now</small></div>
                  </div>
                </article>
              </div>
            </div>
          </div>
        </div>

        <div class="floating-card floating-card--payroll">
          <div class="ring"><span>92%</span></div>
          <div><strong>Payroll ready</strong><small>All approvals complete</small></div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { QBtn, QIcon } from 'quasar';
</script>
