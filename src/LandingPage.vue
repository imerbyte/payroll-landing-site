<template>
  <div class="landing-page">
    <section class="hero">
      <div class="hero-orb hero-orb--one" />
      <div class="hero-orb hero-orb--two" />

      <div class="hero-inner">
        <div class="hero-copy">
          <div class="eyebrow">
            <span class="eyebrow-mark"><q-icon name="verified" /></span>
            Built for Belizean organizations
          </div>
          <h1>Put people at the <span>heart of work.</span></h1>
          <p>
            Payroll, employee records, leave, recruitment, and performance in one beautifully
            connected platform.
          </p>
          <div class="hero-actions">
            <q-btn
              unelevated
              no-caps
              href="/login"
              label="Sign in to People & Payroll"
              icon-right="arrow_forward"
              class="primary-cta"
            />
            <q-btn outline no-caps href="/careers" label="View open roles" class="secondary-cta" />
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
            <span class="floating-icon"><q-icon name="event_available" /></span>
            <div><strong>Leave approved</strong><small>Alisha Morgan</small></div>
          </div>

          <div class="product-window">
            <div class="window-header">
              <div class="window-brand">
                <span><q-icon name="groups" /></span>
                People &amp; Payroll
              </div>
              <div class="window-actions">
                <q-icon name="notifications_none" />
                <span>JM</span>
              </div>
            </div>

            <div class="window-layout">
              <aside>
                <div class="nav-active"><q-icon name="grid_view" /><span>Overview</span></div>
                <div><q-icon name="badge" /><span>People</span></div>
                <div><q-icon name="payments" /><span>Payroll</span></div>
                <div><q-icon name="event_available" /><span>Leave</span></div>
                <div><q-icon name="insights" /><span>Reports</span></div>
              </aside>

              <main>
                <div class="dashboard-title">
                  <div>
                    <small>Monday, 23 November</small>
                    <h2>Good morning, Jamie</h2>
                  </div>
                  <button type="button">Run payroll <q-icon name="arrow_forward" /></button>
                </div>

                <div class="metric-grid">
                  <article>
                    <span class="metric-icon metric-icon--blue"><q-icon name="groups" /></span>
                    <small>Employees</small>
                    <strong>248</strong>
                    <em>+12 this year</em>
                  </article>
                  <article>
                    <span class="metric-icon metric-icon--orange"><q-icon name="account_balance_wallet" /></span>
                    <small>Next payroll</small>
                    <strong>$86.2k</strong>
                    <em>Due in 4 days</em>
                  </article>
                  <article>
                    <span class="metric-icon metric-icon--green"><q-icon name="event_busy" /></span>
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
              </main>
            </div>
          </div>

          <div class="floating-card floating-card--payroll">
            <div class="ring"><span>92%</span></div>
            <div><strong>Payroll ready</strong><small>All approvals complete</small></div>
          </div>
        </div>
      </div>
    </section>

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
            <span class="platform-list-icon"><q-icon :name="item.icon" /></span>
            <div><strong>{{ item.title }}</strong><small>{{ item.detail }}</small></div>
          </div>
        </div>
      </div>
      <div class="platform-art">
        <div class="platform-art__glow" />
        <div class="people-card">
          <div class="people-card__header">
            <div><small>PEOPLE DIRECTORY</small><strong>Your team, at a glance</strong></div>
            <q-icon name="more_horiz" />
          </div>
          <div v-for="person in teamPreview" :key="person.name" class="people-row">
            <span class="people-avatar" :class="person.color">{{ person.initials }}</span>
            <div><strong>{{ person.name }}</strong><small>{{ person.role }}</small></div>
            <span class="people-status" :class="person.statusClass">{{ person.status }}</span>
          </div>
          <div class="people-card__footer"><q-icon name="lock" /> Private employee information, in one secure place</div>
        </div>
        <div class="payroll-chip"><q-icon name="task_alt" /> Payroll and people data in sync</div>
      </div>
    </section>

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
          <div class="feature-icon"><q-icon name="payments" /></div>
          <h3>Confident payroll</h3>
          <p>Process earnings, deductions, taxes, and reports with fewer manual steps.</p>
          <q-btn flat no-caps label="Explore payroll" icon-right="arrow_forward" href="#platform" />
        </article>
        <article class="feature-card">
          <span class="feature-number">02</span>
          <div class="feature-icon"><q-icon name="badge" /></div>
          <h3>Complete employee records</h3>
          <p>Keep profiles, documents, contracts, and employment history together.</p>
        </article>
        <article class="feature-card">
          <span class="feature-number">03</span>
          <div class="feature-icon"><q-icon name="event_available" /></div>
          <h3>Time and leave</h3>
          <p>Coordinate attendance, requests, approvals, schedules, and availability.</p>
        </article>
        <article class="feature-card">
          <span class="feature-number">04</span>
          <div class="feature-icon"><q-icon name="how_to_reg" /></div>
          <h3>Hiring without friction</h3>
          <p>Publish vacancies and move candidates through a clear recruitment flow.</p>
        </article>
        <article class="feature-card">
          <span class="feature-number">05</span>
          <div class="feature-icon"><q-icon name="trending_up" /></div>
          <h3>Growth and performance</h3>
          <p>Bring goals, reviews, and employee development into the people conversation.</p>
        </article>
      </div>
    </section>

    <section id="industries" class="industries-section">
      <div class="industries-heading">
        <span class="section-kicker">MADE FOR THE WAY YOU WORK</span>
        <h2>One platform. Different kinds of teams.</h2>
        <p>Flexible people operations for organizations at every stage and across every sector.</p>
      </div>
      <div class="industry-grid">
        <article v-for="industry in industries" :key="industry.title" class="industry-card">
          <span class="industry-icon"><q-icon :name="industry.icon" /></span>
          <h3>{{ industry.title }}</h3>
          <p>{{ industry.detail }}</p>
        </article>
      </div>
    </section>

    <section class="why-section">
      <div class="why-visual">
        <div class="why-visual__sun" />
        <div class="why-quote-card">
          <span class="quote-mark">“</span>
          <p>Less time chasing paperwork. More time supporting people.</p>
          <div class="quote-caption"><span class="quote-dot" /> A better way to work, together</div>
        </div>
      </div>
      <div class="why-copy">
        <span class="section-kicker">WHY PEOPLE &amp; PAYROLL</span>
        <h2>Practical tools for the work that matters.</h2>
        <p>
          The best HR technology should feel clear, dependable, and close to your organization’s
          real needs.
        </p>
        <div class="why-points">
          <div><q-icon name="check_circle" /><span><strong>Belize-focused workflows</strong><small>Payroll tools and reporting designed around local requirements.</small></span></div>
          <div><q-icon name="check_circle" /><span><strong>One dependable source</strong><small>Keep employee details and important documents together.</small></span></div>
          <div><q-icon name="check_circle" /><span><strong>Less routine follow-up</strong><small>Give requests, reviews, and approvals a clear path forward.</small></span></div>
        </div>
      </div>
    </section>

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
          <q-btn flat no-caps label="Explore solutions" icon-right="arrow_forward" @click="scrollToSection('solutions')" />
        </article>
        <article class="resource-card">
          <span>FOR CANDIDATES</span>
          <h3>Find your next opportunity.</h3>
          <p>Browse current vacancies and learn more about joining a team.</p>
          <q-btn flat no-caps label="View open roles" icon-right="arrow_forward" href="/careers" />
        </article>
        <article class="resource-card resource-card--navy">
          <span>FOR YOUR TEAM</span>
          <h3>Pick up where you left off.</h3>
          <p>Sign in to manage your work, people, and payroll tasks.</p>
          <q-btn flat no-caps label="Go to sign in" icon-right="arrow_forward" href="/login" />
        </article>
      </div>
    </section>

    <section class="closing-cta">
      <div class="closing-cta__pattern" />
      <div>
        <span>MAKE WORK BETTER FOR EVERYONE</span>
        <h2>Bring your people operations together.</h2>
        <p>Take the next step toward a more connected workday.</p>
      </div>
      <div class="closing-cta__actions">
        <q-btn
          unelevated
          no-caps
          href="/login"
          label="Sign in to get started"
          icon-right="arrow_forward"
          class="closing-primary"
        />
        <q-btn outline no-caps href="/careers" label="Explore careers" class="closing-secondary" />
      </div>
    </section>

    <footer class="site-footer">
      <q-btn flat no-caps href="/" class="footer-brand">
        <img src="/belize-coat-of-arms.png" alt="" />
        <span>People &amp; Payroll</span>
      </q-btn>
      <span class="footer-note">Built for better work in Belize.</span>
      <nav aria-label="Footer navigation">
        <q-btn flat no-caps href="/careers" label="Careers" />
        <q-btn flat no-caps href="/login" label="Sign in" />
      </nav>
      <small>© {{ currentYear }} People &amp; Payroll</small>
    </footer>
  </div>
</template>

<script setup>
const currentYear = new Date().getFullYear();

const platformItems = [
  {
    icon: 'badge',
    title: 'A complete employee picture',
    detail: 'Keep essential records, documents, and history connected.',
  },
  {
    icon: 'payments',
    title: 'Payroll with context',
    detail: 'Bring employee and pay information into the same workflow.',
  },
  {
    icon: 'task_alt',
    title: 'Clear steps from request to approval',
    detail: 'Give everyday people processes a visible, consistent path.',
  },
];

const teamPreview = [
  { initials: 'AM', name: 'Alisha Morgan', role: 'People & Culture', status: 'At work', statusClass: 'available', color: 'avatar--peach' },
  { initials: 'DR', name: 'David Reyes', role: 'Finance', status: 'On leave', statusClass: 'away', color: 'avatar--gold' },
  { initials: 'MS', name: 'Maria Salazar', role: 'Operations', status: 'At work', statusClass: 'available', color: 'avatar--green' },
];

const industries = [
  {
    icon: 'account_balance',
    title: 'Public service',
    detail: 'Organize people records and approvals across structured teams.',
  },
  {
    icon: 'school',
    title: 'Education',
    detail: 'Coordinate employee information, schedules, and pay cycles.',
  },
  {
    icon: 'volunteer_activism',
    title: 'Nonprofits',
    detail: 'Spend less time coordinating admin and more time on your mission.',
  },
  {
    icon: 'storefront',
    title: 'Growing businesses',
    detail: 'Build consistent people processes as your team grows.',
  },
];

function scrollToSection(id) {
  document.getElementById(id)?.scrollIntoView({ behavior: 'smooth', block: 'start' });
}
</script>

<style scoped>
.landing-page {
  min-height: 100%;
  padding: 0;
  background: #fffaf5;
  overflow-x: hidden;
}

.hero {
  min-height: 680px;
  position: relative;
  overflow: hidden;
  background:
    radial-gradient(circle at 92% 18%, #f6eee7, transparent 16rem),
    linear-gradient(135deg, #fff8f0 0%, #fffaf5 58%, #fdf1e4 100%);
}

.hero-orb {
  position: absolute;
  border-radius: 50%;
  pointer-events: none;
}

.hero-orb--one {
  width: 460px;
  height: 460px;
  right: -260px;
  bottom: -280px;
  border: 1px solid rgba(23, 50, 77, 0.12);
  box-shadow: 0 0 0 58px rgba(23, 50, 77, 0.025), 0 0 0 116px rgba(23, 50, 77, 0.018);
}

.hero-orb--two {
  width: 12px;
  height: 12px;
  left: 4%;
  bottom: 12%;
  background: var(--q-primary);
  box-shadow: 34px -22px 0 -4px #b7c8d2, -18px -58px 0 -5px #dce5e9;
}

.hero-inner {
  width: min(1180px, calc(100% - 40px));
  min-height: 680px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: minmax(380px, 460px) minmax(520px, 660px);
  align-items: center;
  gap: 60px;
  position: relative;
  z-index: 1;
}

.hero-copy {
  padding: 54px 0;
}

.eyebrow {
  display: inline-flex;
  align-items: center;
  gap: 9px;
  margin-bottom: 20px;
  color: var(--q-primary);
  font-size: 12px;
  font-weight: 850;
  letter-spacing: 0.09em;
  text-transform: uppercase;
}

.eyebrow-mark {
  width: 30px;
  height: 30px;
  display: inline-flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: var(--q-primary);
  color: #fff;
}

.eyebrow-mark :deep(.q-icon) {
  font-size: 17px;
}

.hero h1 {
  max-width: 460px;
  margin: 0;
  color: #17324d;
  font-size: clamp(48px, 5vw, 70px);
  line-height: 0.98;
  letter-spacing: -0.055em;
  font-weight: 820;
}

.hero h1 span {
  color: var(--q-primary);
}

.hero-copy > p {
  max-width: 440px;
  margin: 24px 0 28px;
  color: #66778a;
  font-size: 18px;
  line-height: 1.65;
}

.hero-actions {
  display: flex;
  gap: 12px;
}

.primary-cta,
.secondary-cta {
  height: 52px;
  border-radius: 7px;
  padding: 0 18px;
  font-size: 14px;
  font-weight: 800;
}

.primary-cta {
  background: var(--q-primary);
  color: #fff;
  box-shadow: 0 14px 30px rgba(23, 50, 77, 0.16);
}

.secondary-cta {
  border-color: #dfe5e9;
  color: #17324d;
  background: rgba(255, 255, 255, 0.55);
}

.proof-row {
  display: flex;
  gap: 28px;
  margin-top: 28px;
}

.proof-row div {
  display: grid;
  gap: 2px;
  padding-right: 28px;
  border-right: 1px solid #e5ddd4;
}

.proof-row div:last-child {
  border-right: 0;
}

.proof-row strong {
  color: #17324d;
  font-size: 14px;
}

.proof-row span {
  color: #8a99a7;
  font-size: 11px;
}

.product-stage {
  height: 530px;
  position: relative;
  display: flex;
  align-items: center;
}

.product-window {
  width: 660px;
  height: 470px;
  overflow: hidden;
  border: 1px solid #eadfd4;
  border-radius: 14px;
  background: #fff;
  box-shadow: 0 34px 80px rgba(96, 63, 34, 0.16);
  transform: perspective(1400px) rotateY(-2deg) rotateZ(0.2deg);
}

.window-header {
  height: 52px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 14px;
  border-bottom: 1px solid #f0ebe6;
  color: #17324d;
  font-size: 12px;
  font-weight: 800;
}

.window-brand,
.window-actions {
  display: flex;
  align-items: center;
  gap: 8px;
}

.window-brand > span {
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 7px;
  background: var(--q-primary);
  color: #fff;
}

.window-actions :deep(.q-icon) {
  color: #91a0ad;
  margin-right: 4px;
}

.window-actions > span {
  width: 30px;
  height: 30px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: #edf3f6;
  color: #4d7186;
  font-size: 9px;
}

.window-layout {
  height: calc(100% - 52px);
  display: grid;
  grid-template-columns: 128px 1fr;
}

.window-layout aside {
  padding: 16px 9px;
  border-right: 1px solid #f0ebe6;
  background: #fdfbf8;
}

.window-layout aside div {
  height: 38px;
  display: flex;
  align-items: center;
  gap: 8px;
  margin-bottom: 4px;
  padding: 0 9px;
  border-radius: 7px;
  color: #87949f;
  font-size: 10px;
  font-weight: 700;
}

.window-layout aside div :deep(.q-icon) {
  font-size: 16px;
}

.window-layout aside .nav-active {
  background: #f3f5f6;
  color: var(--q-primary);
}

.window-layout main {
  min-width: 0;
  padding: 20px;
  background: #f8f9f8;
}

.dashboard-title {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 12px;
}

.dashboard-title small {
  color: #9aa5ad;
  font-size: 8px;
}

.dashboard-title h2 {
  margin: 2px 0 0;
  color: #17324d;
  font-size: 15px;
  line-height: 1.2;
}

.dashboard-title button {
  height: 34px;
  display: flex;
  align-items: center;
  gap: 6px;
  border: 0;
  border-radius: 6px;
  padding: 0 11px;
  background: var(--q-primary);
  color: #fff;
  font-size: 9px;
  font-weight: 800;
}

.dashboard-title button :deep(.q-icon) {
  font-size: 14px;
}

.metric-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 9px;
  margin-bottom: 9px;
}

.metric-grid article {
  min-height: 108px;
  position: relative;
  padding: 12px;
  border: 1px solid #eeece8;
  border-radius: 8px;
  background: #fff;
}

.metric-icon {
  position: absolute;
  right: 10px;
  top: 10px;
  width: 32px;
  height: 32px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
}

.metric-icon :deep(.q-icon) {
  font-size: 16px;
}

.metric-icon--blue { background: #edf4f7; color: #4d7186; }
.metric-icon--orange { background: #f3f5f6; color: var(--q-primary); }
.metric-icon--green { background: #e7f3ed; color: #4b9272; }

.metric-grid small,
.metric-grid strong,
.metric-grid em {
  display: block;
}

.metric-grid small {
  color: #95a1aa;
  font-size: 8px;
}

.metric-grid strong {
  margin-top: 9px;
  color: #17324d;
  font-size: 19px;
}

.metric-grid em {
  margin-top: 7px;
  color: #91a0aa;
  font-size: 7px;
  font-style: normal;
}

.dashboard-grid {
  display: grid;
  grid-template-columns: 1.55fr 1fr;
  gap: 9px;
}

.chart-panel,
.activity-panel {
  height: 208px;
  border: 1px solid #eeece8;
  border-radius: 8px;
  background: #fff;
  padding: 12px;
}

.panel-heading {
  display: flex;
  align-items: flex-start;
  justify-content: space-between;
}

.panel-heading small,
.panel-heading strong {
  display: block;
}

.panel-heading small {
  color: #9aa5ad;
  font-size: 7px;
  text-transform: uppercase;
}

.panel-heading strong {
  color: #17324d;
  font-size: 12px;
  margin-top: 3px;
}

.panel-heading > span {
  color: #9aa5ad;
  font-size: 7px;
}

.chart {
  height: 150px;
  margin-top: 5px;
  background: repeating-linear-gradient(to bottom, #f1f2ef 0, #f1f2ef 1px, transparent 1px, transparent 37px);
}

.chart svg {
  width: 100%;
  height: 145px;
}

.chart-area { fill: url(#payrollArea); }
.chart-line { fill: none; stroke: var(--q-primary); stroke-width: 3; stroke-linecap: round; }

.activity-row {
  display: flex;
  align-items: center;
  gap: 8px;
  padding: 9px 0;
  border-bottom: 1px solid #f1eee9;
}

.activity-row:last-child {
  border-bottom: 0;
}

.avatar {
  width: 28px;
  height: 28px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  color: #fff;
  font-size: 8px;
  font-weight: 800;
}

.avatar--peach { background: #dd9072; }
.avatar--gold { background: #d3a84d; }
.avatar--green { background: #67a18a; }

.activity-row strong,
.activity-row small {
  display: block;
}

.activity-row strong {
  color: #526578;
  font-size: 8px;
}

.activity-row small {
  margin-top: 2px;
  color: #9da8ae;
  font-size: 7px;
}

.floating-card {
  position: absolute;
  z-index: 3;
  display: flex;
  align-items: center;
  gap: 10px;
  border: 1px solid #eee5dc;
  border-radius: 10px;
  background: rgba(255, 255, 255, 0.96);
  box-shadow: 0 14px 38px rgba(91, 62, 37, 0.16);
}

.floating-card strong,
.floating-card small {
  display: block;
}

.floating-card strong {
  color: #17324d;
  font-size: 10px;
}

.floating-card small {
  margin-top: 2px;
  color: #91a0aa;
  font-size: 8px;
}

.floating-card--leave {
  left: -24px;
  bottom: 58px;
  padding: 10px 13px 10px 10px;
}

.floating-icon {
  width: 36px;
  height: 36px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 8px;
  background: #e7f3ed;
  color: #4b9272;
}

.floating-card--payroll {
  right: -18px;
  top: 58px;
  padding: 8px 12px 8px 8px;
}

.ring {
  width: 42px;
  height: 42px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  background: conic-gradient(var(--q-primary) 92%, #f3eee8 0);
  position: relative;
}

.ring::after {
  content: '';
  position: absolute;
  inset: 5px;
  border-radius: 50%;
  background: #fff;
}

.ring span {
  position: relative;
  z-index: 1;
  color: #17324d;
  font-size: 8px;
  font-weight: 800;
}

.stage-spark {
  position: absolute;
  z-index: 2;
  width: 7px;
  height: 7px;
  border-radius: 50%;
  background: var(--q-primary);
}

.stage-spark--one {
  right: 10px;
  bottom: 20px;
}

.stage-spark--two {
  left: 70px;
  top: 18px;
  background: var(--q-secondary);
  box-shadow: 18px 12px 0 -2px #dce5e9;
}

.features {
  width: min(1180px, calc(100% - 40px));
  margin: 0 auto;
  padding: 76px 0 88px;
}

.features-heading {
  display: grid;
  grid-template-columns: 1fr 340px;
  align-items: end;
  gap: 40px;
  margin-bottom: 36px;
}

.features-heading span {
  color: var(--q-primary);
  font-size: 11px;
  font-weight: 850;
  letter-spacing: 0.12em;
}

.features-heading h2 {
  margin: 8px 0 0;
  color: #17324d;
  font-size: 44px;
  line-height: 1.05;
  letter-spacing: -0.04em;
}

.features-heading p {
  margin: 0 0 4px;
  color: #738293;
  font-size: 15px;
  line-height: 1.65;
}

.feature-grid {
  display: grid;
  grid-template-columns: 1.25fr repeat(3, 1fr);
  gap: 14px;
}

.feature-card {
  min-height: 260px;
  position: relative;
  padding: 24px;
  border: 1px solid #eee7df;
  border-radius: 12px;
  background: #fff;
}

.feature-card--featured {
  background: #17324d;
  border-color: #17324d;
  color: #fff;
}

.feature-number {
  position: absolute;
  right: 18px;
  top: 18px;
  color: #cbd2d7;
  font-size: 10px;
  font-weight: 800;
}

.feature-card--featured .feature-number {
  color: #9fb1bf;
}

.feature-icon {
  width: 46px;
  height: 46px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  background: #fff1e5;
  color: var(--q-primary);
}

.feature-card--featured .feature-icon {
  background: var(--q-primary);
  color: #fff;
}

.feature-icon :deep(.q-icon) {
  font-size: 22px;
}

.feature-card h3 {
  margin: 38px 0 8px;
  color: #17324d;
  font-size: 18px;
  line-height: 1.2;
}

.feature-card--featured h3 {
  color: #fff;
}

.feature-card p {
  margin: 0;
  color: #7b8995;
  font-size: 13px;
  line-height: 1.55;
}

.feature-card--featured p {
  color: #cad6de;
}

.feature-card .q-btn {
  margin: 18px 0 0 -8px;
  color: var(--q-secondary);
  font-size: 12px;
  font-weight: 800;
}

.platform-section,
.features,
.industries-section,
.why-section,
.resources-section {
  scroll-margin-top: 76px;
}

.platform-section {
  width: min(1180px, calc(100% - 40px));
  min-height: 590px;
  margin: 0 auto;
  padding: 88px 0;
  display: grid;
  grid-template-columns: minmax(0, 0.9fr) minmax(0, 1.1fr);
  align-items: center;
  gap: 72px;
}

.section-kicker {
  color: var(--q-primary);
  font-size: 11px;
  font-weight: 850;
  letter-spacing: 0.12em;
}

.platform-copy h2,
.industries-heading h2,
.why-copy h2,
.resources-heading h2 {
  margin: 12px 0 14px;
  color: #17324d;
  font-size: 42px;
  line-height: 1.06;
  letter-spacing: -0.045em;
}

.platform-copy > p,
.industries-heading > p,
.why-copy > p,
.resources-heading > p {
  color: #738293;
  font-size: 15px;
  line-height: 1.7;
}

.platform-list {
  display: grid;
  gap: 18px;
  margin-top: 30px;
}

.platform-list-item {
  display: flex;
  align-items: center;
  gap: 12px;
}

.platform-list-icon {
  width: 42px;
  height: 42px;
  flex: 0 0 42px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  background: #f3f5f6;
  color: var(--q-primary);
}

.platform-list-icon :deep(.q-icon) {
  font-size: 20px;
}

.platform-list-item strong,
.platform-list-item small {
  display: block;
}

.platform-list-item strong {
  color: #17324d;
  font-size: 14px;
}

.platform-list-item small {
  margin-top: 4px;
  color: #87949f;
  font-size: 12px;
  line-height: 1.45;
}

.platform-art {
  min-height: 410px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 18px;
  background: #fff2e5;
  overflow: hidden;
}

.platform-art__glow {
  position: absolute;
  width: 310px;
  height: 310px;
  right: -80px;
  top: -105px;
  border: 1px solid rgba(23, 50, 77, 0.14);
  border-radius: 50%;
  box-shadow: 0 0 0 42px rgba(23, 50, 77, 0.035), 0 0 0 84px rgba(23, 50, 77, 0.02);
}

.people-card {
  z-index: 1;
  width: min(420px, calc(100% - 54px));
  padding: 20px 20px 0;
  border: 1px solid #eee8e2;
  border-radius: 13px;
  background: #fff;
  box-shadow: 0 24px 54px rgba(91, 62, 37, 0.15);
}

.people-card__header {
  display: flex;
  justify-content: space-between;
  padding-bottom: 14px;
  border-bottom: 1px solid #f0ede9;
}

.people-card__header small,
.people-card__header strong {
  display: block;
}

.people-card__header small {
  color: var(--q-primary);
  font-size: 8px;
  font-weight: 850;
  letter-spacing: 0.1em;
}

.people-card__header strong {
  margin-top: 5px;
  color: #17324d;
  font-size: 15px;
}

.people-card__header > :deep(.q-icon) {
  color: #87949f;
}

.people-row {
  min-height: 65px;
  display: flex;
  align-items: center;
  gap: 10px;
  border-bottom: 1px solid #f3f0ec;
}

.people-avatar {
  width: 34px;
  height: 34px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 50%;
  color: #fff;
  font-size: 9px;
  font-weight: 800;
}

.people-row > div {
  min-width: 0;
  flex: 1;
}

.people-row strong,
.people-row small {
  display: block;
}

.people-row strong {
  color: #334e63;
  font-size: 11px;
}

.people-row small {
  margin-top: 3px;
  color: #94a0a9;
  font-size: 9px;
}

.people-status {
  padding: 5px 7px;
  border-radius: 999px;
  font-size: 8px;
  font-weight: 750;
}

.people-status.available {
  background: #e8f4ec;
  color: #4a8f69;
}

.people-status.away {
  background: #fff2e2;
  color: #c57a33;
}

.people-card__footer {
  display: flex;
  align-items: center;
  gap: 6px;
  padding: 13px 0;
  color: #8d999f;
  font-size: 8px;
}

.people-card__footer :deep(.q-icon) {
  color: #63917b;
  font-size: 13px;
}

.payroll-chip {
  position: absolute;
  z-index: 2;
  right: 22px;
  bottom: 30px;
  display: flex;
  align-items: center;
  gap: 7px;
  padding: 11px 14px;
  border: 1px solid #eee8e2;
  border-radius: 8px;
  background: #fff;
  box-shadow: 0 10px 24px rgba(91, 62, 37, 0.12);
  color: #506b60;
  font-size: 9px;
  font-weight: 750;
}

.payroll-chip :deep(.q-icon) {
  color: #4b9272;
  font-size: 16px;
}

.industries-section {
  padding: 78px max(20px, calc((100% - 1180px) / 2)) 84px;
  background: #f5f2ed;
}

.industries-heading {
  max-width: 720px;
  margin-bottom: 32px;
}

.industries-heading h2 {
  margin-bottom: 10px;
}

.industries-heading > p {
  max-width: 550px;
  margin: 0;
}

.industry-grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 14px;
}

.industry-card {
  min-height: 200px;
  padding: 22px;
  border: 1px solid #e8e2d9;
  border-radius: 11px;
  background: #fffdfa;
}

.industry-icon {
  width: 42px;
  height: 42px;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 10px;
  background: #f3f5f6;
  color: var(--q-primary);
}

.industry-icon :deep(.q-icon) {
  font-size: 21px;
}

.industry-card h3 {
  margin: 20px 0 7px;
  color: #17324d;
  font-size: 16px;
}

.industry-card p {
  margin: 0;
  color: #7b8995;
  font-size: 12px;
  line-height: 1.55;
}

.why-section {
  width: min(1180px, calc(100% - 40px));
  min-height: 570px;
  margin: 0 auto;
  padding: 88px 0;
  display: grid;
  grid-template-columns: 1fr 0.9fr;
  align-items: center;
  gap: 90px;
}

.why-visual {
  height: 380px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: center;
  border-radius: 16px;
  overflow: hidden;
  background: linear-gradient(145deg, #17324d, #20546a);
}

.why-visual__sun {
  position: absolute;
  width: 330px;
  height: 330px;
  left: -90px;
  bottom: -180px;
  border-radius: 50%;
  background: var(--q-primary);
  box-shadow: 0 0 0 38px rgba(23, 50, 77, 0.10), 0 0 0 76px rgba(23, 50, 77, 0.06);
}

.why-quote-card {
  z-index: 1;
  width: min(370px, calc(100% - 40px));
  padding: 28px;
  border: 1px solid rgba(255, 255, 255, 0.35);
  border-radius: 12px;
  background: rgba(255, 255, 255, 0.96);
  box-shadow: 0 24px 60px rgba(5, 23, 38, 0.22);
}

.quote-mark {
  color: var(--q-primary);
  font-family: Georgia, serif;
  font-size: 60px;
  line-height: 0.7;
}

.why-quote-card p {
  margin: 18px 0 26px;
  color: #17324d;
  font-size: 25px;
  font-weight: 750;
  line-height: 1.2;
  letter-spacing: -0.035em;
}

.quote-caption {
  display: flex;
  align-items: center;
  gap: 8px;
  color: #82909b;
  font-size: 10px;
  font-weight: 700;
}

.quote-dot {
  width: 8px;
  height: 8px;
  border-radius: 50%;
  background: var(--q-primary);
}

.why-copy h2 {
  margin-bottom: 12px;
}

.why-copy > p {
  margin: 0;
}

.why-points {
  display: grid;
  gap: 19px;
  margin-top: 28px;
}

.why-points > div {
  display: flex;
  align-items: flex-start;
  gap: 11px;
}

.why-points > div > :deep(.q-icon) {
  margin-top: 2px;
  color: #4b9272;
  font-size: 19px;
}

.why-points strong,
.why-points small {
  display: block;
}

.why-points strong {
  color: #29465b;
  font-size: 13px;
}

.why-points small {
  margin-top: 4px;
  color: #87949f;
  font-size: 11px;
  line-height: 1.45;
}

.resources-section {
  padding: 76px max(20px, calc((100% - 1180px) / 2)) 84px;
  background: #fff;
}

.resources-heading {
  display: flex;
  align-items: end;
  justify-content: space-between;
  gap: 36px;
  margin-bottom: 30px;
}

.resources-heading h2 {
  margin-bottom: 0;
}

.resources-heading > p {
  max-width: 350px;
  margin: 0 0 4px;
}

.resource-grid {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 14px;
}

.resource-card {
  min-height: 245px;
  padding: 24px;
  border: 1px solid #eee7df;
  border-radius: 11px;
  background: #fffaf5;
}

.resource-card--orange {
  background: #f3f5f6;
  border-color: #e4e9ec;
}

.resource-card--navy {
  background: #17324d;
  border-color: #17324d;
}

.resource-card > span {
  color: var(--q-primary);
  font-size: 9px;
  font-weight: 850;
  letter-spacing: 0.1em;
}

.resource-card--navy > span {
  color: var(--q-secondary);
}

.resource-card h3 {
  max-width: 280px;
  margin: 20px 0 9px;
  color: #17324d;
  font-size: 20px;
  line-height: 1.2;
}

.resource-card--navy h3 {
  color: #fff;
}

.resource-card p {
  min-height: 42px;
  margin: 0;
  color: #738293;
  font-size: 12px;
  line-height: 1.5;
}

.resource-card--navy p {
  color: #cad6de;
}

.resource-card .q-btn {
  margin: 15px 0 0 -8px;
  color: var(--q-primary);
  font-size: 11px;
  font-weight: 800;
}

.resource-card--navy .q-btn {
  color: var(--q-secondary);
}

.closing-cta {
  min-height: 290px;
  position: relative;
  display: flex;
  align-items: center;
  justify-content: space-between;
  gap: 40px;
  overflow: hidden;
  padding: 56px max(20px, calc((100% - 1180px) / 2));
  background: #17324d;
}

.closing-cta__pattern {
  position: absolute;
  right: -120px;
  top: -260px;
  width: 520px;
  height: 520px;
  border: 1px solid rgba(255, 255, 255, 0.14);
  border-radius: 50%;
  box-shadow: 0 0 0 58px rgba(255, 255, 255, 0.035), 0 0 0 116px rgba(255, 255, 255, 0.025);
}

.closing-cta > div:not(.closing-cta__pattern) {
  position: relative;
  z-index: 1;
}

.closing-cta > div:first-of-type > span {
  color: var(--q-secondary);
  font-size: 10px;
  font-weight: 850;
  letter-spacing: 0.13em;
}

.closing-cta h2 {
  max-width: 600px;
  margin: 10px 0 8px;
  color: #fff;
  font-size: 40px;
  line-height: 1.05;
  letter-spacing: -0.04em;
}

.closing-cta p {
  margin: 0;
  color: #cad6de;
  font-size: 14px;
}

.closing-cta__actions {
  display: flex;
  flex-shrink: 0;
  gap: 10px;
}

.closing-primary,
.closing-secondary {
  height: 48px;
  padding: 0 16px;
  border-radius: 7px;
  font-size: 12px;
  font-weight: 800;
}

.closing-primary {
  background: var(--q-primary);
  color: #fff;
}

.closing-secondary {
  border-color: rgba(255, 255, 255, 0.45);
  color: #fff;
}

.site-footer {
  min-height: 92px;
  width: min(1180px, calc(100% - 40px));
  margin: 0 auto;
  display: flex;
  align-items: center;
  gap: 22px;
  color: #8a969f;
}

.footer-brand {
  padding: 4px 0;
  color: #17324d;
  font-size: 13px;
  font-weight: 800;
}

.footer-brand img {
  width: 28px;
  height: 28px;
  margin-right: 8px;
  object-fit: contain;
}

.footer-note {
  color: #8a969f;
  font-size: 10px;
}

.site-footer nav {
  display: flex;
  gap: 4px;
  margin-left: auto;
}

.site-footer nav :deep(.q-btn) {
  color: #637586;
  font-size: 11px;
}

.site-footer > small {
  color: #9ba5ac;
  font-size: 10px;
}

@media (max-width: 1120px) {
  .hero-inner {
    grid-template-columns: minmax(340px, 420px) minmax(460px, 560px);
    gap: 30px;
  }

  .product-window {
    width: 560px;
  }

  .platform-section {
    gap: 36px;
  }

  .feature-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

@media (max-width: 900px) {
  .hero-inner {
    grid-template-columns: minmax(0, 1fr);
    width: min(680px, calc(100% - 32px));
    gap: 24px;
  }

  .hero-copy,
  .product-stage {
    min-width: 0;
    width: 100%;
  }

  .hero-copy {
    text-align: center;
    padding: 48px 0 18px;
  }

  .hero h1,
  .hero-copy > p {
    margin-left: auto;
    margin-right: auto;
  }

  .hero-actions,
  .proof-row {
    justify-content: center;
  }

  .product-stage {
    width: 680px;
    max-width: 100%;
  }

  .features-heading {
    grid-template-columns: 1fr;
  }

  .platform-section,
  .why-section {
    width: min(680px, calc(100% - 32px));
    grid-template-columns: 1fr;
    gap: 38px;
  }

  .platform-section {
    padding: 64px 0;
  }

  .platform-art {
    min-height: 380px;
  }

  .why-section {
    padding: 64px 0;
  }

  .why-visual {
    height: 330px;
  }

  .industry-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .resource-grid {
    grid-template-columns: repeat(2, 1fr);
  }

  .resource-card:last-child {
    grid-column: 1 / -1;
  }

  .closing-cta {
    align-items: flex-start;
    flex-direction: column;
  }

  .site-footer {
    flex-wrap: wrap;
    padding: 20px 0;
  }
}

@media (max-width: 620px) {
  .hero-inner {
    width: calc(100% - 32px);
  }

  .hero h1 {
    font-size: 43px;
  }

  .hero-copy > p {
    font-size: 16px;
  }

  .hero-actions {
    flex-direction: column;
  }

  .primary-cta,
  .secondary-cta {
    width: 100%;
  }

  .proof-row {
    gap: 12px;
  }

  .proof-row div {
    padding-right: 12px;
  }

  .product-stage {
    height: 430px;
  }

  .product-window {
    width: 100%;
    height: 400px;
  }

  .window-layout {
    grid-template-columns: 48px minmax(0, 1fr);
  }

  .window-layout aside {
    padding: 12px 4px;
  }

  .window-layout aside div {
    justify-content: center;
    padding: 0 4px;
  }

  .window-layout aside div span {
    display: none;
  }

  .window-layout main {
    padding: 12px 8px;
  }

  .metric-grid {
    gap: 4px;
  }

  .metric-grid article {
    min-height: 92px;
    padding: 8px;
  }

  .metric-icon {
    width: 26px;
    height: 26px;
    top: 7px;
    right: 6px;
  }

  .dashboard-grid {
    grid-template-columns: 1fr;
  }

  .activity-panel {
    display: none;
  }

  .chart-panel {
    height: 150px;
  }

  .chart {
    height: 95px;
  }

  .chart svg {
    height: 90px;
  }

  .floating-card--leave,
  .floating-card--payroll {
    display: none;
  }

  .features {
    width: calc(100% - 32px);
  }

  .features-heading h2 {
    font-size: 36px;
  }

  .feature-grid {
    grid-template-columns: 1fr;
  }

  .platform-copy h2,
  .industries-heading h2,
  .why-copy h2,
  .resources-heading h2 {
    font-size: 35px;
  }

  .platform-art {
    min-height: 340px;
  }

  .people-card {
    width: calc(100% - 32px);
    padding: 16px 14px 0;
  }

  .people-status {
    display: none;
  }

  .payroll-chip {
    right: 12px;
    bottom: 14px;
  }

  .industries-section,
  .resources-section {
    padding: 56px 16px;
  }

  .industry-grid,
  .resource-grid {
    grid-template-columns: 1fr;
  }

  .resource-card:last-child {
    grid-column: auto;
  }

  .industry-card {
    min-height: 0;
  }

  .resources-heading {
    align-items: flex-start;
    flex-direction: column;
    gap: 12px;
  }

  .why-visual {
    height: 300px;
  }

  .why-quote-card {
    padding: 22px;
  }

  .why-quote-card p {
    font-size: 22px;
  }

  .closing-cta {
    min-height: 0;
    padding: 48px 16px;
  }

  .closing-cta h2 {
    font-size: 34px;
  }

  .closing-cta__actions {
    width: 100%;
    flex-direction: column;
  }

  .closing-primary,
  .closing-secondary {
    width: 100%;
  }

  .site-footer {
    width: calc(100% - 32px);
    gap: 10px 16px;
  }

  .footer-note {
    display: none;
  }

  .site-footer nav {
    margin-left: auto;
  }

  .site-footer > small {
    width: 100%;
  }
}
</style>
