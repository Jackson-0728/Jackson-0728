<style>
:root {
  --bg: #05070c;
  --glass: rgba(255,255,255,.08);
  --border: rgba(255,255,255,.15);
  --text: #f5f7ff;
  --muted: #9aa4c7;
  --accent: #6cf2c2;
}

body {
  background: radial-gradient(circle at top, #0b1020, #05070c 70%);
  color: var(--text);
  font-family: Inter, system-ui, sans-serif;
}

/* HERO */
.hero {
  min-height: 90vh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
}

.hero h1 {
  font-size: clamp(3rem, 8vw, 6rem);
  letter-spacing: -0.03em;
}

.hero span {
  color: var(--accent);
}

.hero p {
  margin-top: 20px;
  color: var(--muted);
  font-size: 1.2rem;
}

/* BUTTON */
.button {
  display: inline-block;
  margin-top: 40px;
  padding: 14px 28px;
  border-radius: 999px;
  background: var(--glass);
  border: 1px solid var(--border);
  backdrop-filter: blur(16px);
  color: white;
  text-decoration: none;
  font-weight: 600;
  transition: transform .3s, background .3s;
}

.button:hover {
  transform: translateY(-4px);
  background: rgba(255,255,255,.15);
}

/* SECTIONS */
.section {
  padding: 120px 6vw;
}

.section h2 {
  font-size: 2.6rem;
  margin-bottom: 60px;
}

/* GRID */
.grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(260px, 1fr));
  gap: 32px;
}

.card {
  padding: 32px;
  border-radius: 24px;
  background: linear-gradient(
    180deg,
    rgba(255,255,255,.12),
    rgba(255,255,255,.03)
  );
  border: 1px solid var(--border);
  backdrop-filter: blur(18px);
  transition: transform .4s;
}

.card:hover {
  transform: translateY(-12px);
}

.card h3 {
  margin-bottom: 12px;
}

.card p {
  color: var(--muted);
  line-height: 1.6;
}

/* CURSOR GLOW */
.cursor {
  position: fixed;
  width: 300px;
  height: 300px;
  background: radial-gradient(circle, rgba(108,242,194,.18), transparent 70%);
  pointer-events: none;
  transform: translate(-50%, -50%);
  z-index: 0;
}
</style>

<div class="cursor"></div>

<div class="hero">
  <div>
    <h1>Jackson <span>Liu</span></h1>
    <p>Creative Technologist · Full-Stack Developer · Founder</p>
    <a class="button" href="https://nexstudio.tech" target="_blank">
      Visit NexStudio
    </a>
  </div>
</div>

---

<div class="section">
  <h2>Selected Work</h2>

  <div class="grid">
    <div class="card">
      <h3>Interactive Websites</h3>
      <p>
        Scroll-driven, cinematic, glassmorphic web experiences with award-level polish.
      </p>
    </div>

    <div class="card">
      <h3>AI Systems</h3>
      <p>
        Conversational AI, computer vision, gesture interfaces, and real-time tools.
      </p>
    </div>

    <div class="card">
      <h3>Creative Research</h3>
      <p>
        Data-driven design grounded in developmental psychology and human behaviour.
      </p>
    </div>
  </div>
</div>

---

<div class="section">
  <h2>Philosophy</h2>

  <div class="grid">
    <div class="card">
      <h3>Design That Moves</h3>
      <p>
        If it doesn’t react, breathe, or respond — it’s not finished.
      </p>
    </div>

    <div class="card">
      <h3>Technology as Storytelling</h3>
      <p>
        Motion, interaction, and systems should communicate intent and emotion.
      </p>
    </div>
  </div>
</div>

---

<footer style="text-align:center; padding:80px 0; color:var(--muted)">
  © 2025 Jackson Liu · Built with intent
</footer>

<script>
const cursor = document.querySelector('.cursor');

window.addEventListener('mousemove', e => {
  cursor.style.left = e.clientX + 'px';
  cursor.style.top = e.clientY + 'px';
});
</script>
