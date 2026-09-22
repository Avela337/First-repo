<template>
  <main style="padding-top: var(--nav-h);">
    <section class="about">
      <div class="container">
        <div class="about-grid">

          <div class="photo-col">
            <div class="photo-card">
              <div class="photo-placeholder">
                <span class="initials">AG</span>
              </div>
              <div class="photo-caption">
                <span class="caption-name">Avela_Gxotiwe.sh</span>
                <span class="caption-sub">Full-Stack Developer · Cape Town</span>
              </div>
            </div>
          </div>

          <div class="content-col">
            <div class="section-label">
              
              About
            </div>

            <h2>Solving Real Problems<br>with Purposeful Code</h2>

            <p class="bio">
              I'm a Full Stack Developer from Cape Town, South Africa, with a passion for building
              software that genuinely makes a difference. Growing up in the Cape, I was always
              drawn to how things work and coding became my way of building things that matter.
              Whether it's architecting a REST API or crafting a responsive Vue frontend, I bring
              the same energy, clean, purposeful, and built to last.
            </p>

            <div class="highlight-cards">
              <div class="h-card">
                <span class="h-title">Full-Stack Development</span>
                <span class="h-sub">Vue 3, Node.js, Express &amp; MySQL</span>
              </div>
              <div class="h-card">
                <span class="h-title">API Integration</span>
                <span class="h-sub">RESTful APIs &amp; JWT authentication</span>
              </div>
            </div>

            <div class="social-links">
              <div class="social-row">
                <span class="s-label">EMAIL:</span>
                <a href="mailto:avelagxotiwe@gmail.com" class="s-link">avelagxotiwe@gmail.com</a>
              </div>
              <div class="social-row">
                <span class="s-label">GITHUB:</span>
                <a href="https://github.com/Avela337" target="_blank" class="s-link">github.com/Avela337</a>
              </div>
              <div class="social-row">
                <span class="s-label">LINKEDIN:</span>
                <a href="https://www.linkedin.com/in/avela-gxotiwe-674a942b9" target="_blank" class="s-link">avela-gxotiwe</a>
              </div>
            </div>
          </div>
        </div>

        <div class="tech-strip">
          <span class="strip-label">TECHNOLOGIES I WORK WITH</span>
          <div class="strip-items">
            <span v-for="tech in techs" :key="tech" class="strip-item">{{ tech }}</span>
          </div>
        </div>
      </div>
    </section>
  </main>
</template>

<script setup>
const techs = ['Vue 3', 'JavaScript', 'Node.js', 'Express', 'PHP', 'MySQL', 'HTML5', 'CSS3', 'Git', 'Vite', 'JWT', 'REST APIs']
</script>

<style scoped>
.about { padding: 72px 0 96px; }
.about-grid { display: grid; grid-template-columns: 360px 1fr; gap: 64px; align-items: start; margin-bottom: 72px; }
.photo-card { border-radius: var(--radius-lg); overflow: hidden; border: 1px solid var(--border-light); }
.photo-placeholder { width: 100%; aspect-ratio: 1/1.1; background: linear-gradient(135deg, #0d2b1e, #1a4a30); display: flex; align-items: center; justify-content: center; }
.initials { font-family: var(--mono); font-size: 4rem; font-weight: 700; color: var(--accent); opacity: 0.7; }
.photo-caption { background: var(--text); padding: 16px 20px; display: flex; flex-direction: column; gap: 4px; }
.caption-name { font-family: var(--mono); font-size: 0.85rem; font-weight: 600; color: #fff; }
.caption-sub { font-size: 0.78rem; color: var(--accent); font-family: var(--mono); }
.content-col h2 { margin-bottom: 20px; margin-top: 8px; }
.bio { font-size: 1rem; margin-bottom: 28px; }
.highlight-cards { display: grid; grid-template-columns: 1fr 1fr; gap: 14px; margin-bottom: 32px; }
.h-card { background: var(--bg-card); border: 1px solid var(--border-light); border-radius: var(--radius); padding: 16px 18px; display: flex; flex-direction: column; gap: 4px; }
.h-title { font-size: 0.9rem; font-weight: 700; color: var(--text); }
.h-sub { font-size: 0.78rem; color: var(--text-muted); }
.social-links { display: flex; flex-direction: column; gap: 10px; }
.social-row { display: flex; align-items: center; gap: 12px; }
.s-label { font-family: var(--mono); font-size: 0.72rem; font-weight: 600; letter-spacing: 0.08em; color: var(--accent); min-width: 80px; }
.s-link { font-size: 0.88rem; color: var(--text-muted); transition: color 0.2s; }
.s-link:hover { color: var(--accent); }
.tech-strip { border-top: 1px solid var(--border-light); padding-top: 40px; display: flex; flex-direction: column; gap: 20px; align-items: center; text-align: center; }
.strip-label { font-family: var(--mono); font-size: 0.7rem; letter-spacing: 0.12em; color: var(--text-faint); }
.strip-items { display: flex; flex-wrap: wrap; gap: 12px 32px; justify-content: center; }
.strip-item { font-size: 1rem; font-weight: 700; color: var(--text-muted); transition: color 0.2s; cursor: default; }
.strip-item:hover { color: var(--accent); }
@media (max-width: 860px) { .about-grid { grid-template-columns: 1fr; gap: 40px; } .highlight-cards { grid-template-columns: 1fr; } }
</style>