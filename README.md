:root {
  --ink: #14171c;
  --orange: #ff5a1f;
  --chalk: #fafafa;
  --steel: #8a94a3;
  --line: #d9dde3;
}

* { box-sizing: border-box; }

html { scroll-behavior: smooth; }

body {
  margin: 0;
  font-family: system-ui, -apple-system, "Segoe UI", Roboto, sans-serif;
  line-height: 1.6;
  color: var(--ink);
  background: var(--chalk);
}

h1, h2, .brand, .btn {
  font-family: "Barlow Condensed", "Arial Narrow", sans-serif;
  font-weight: 800;
  line-height: 1.05;
}

a { color: inherit; }
a:focus-visible { outline: 3px solid var(--orange); outline-offset: 3px; }

.top {
  display: flex;
  justify-content: space-between;
  align-items: center;
  flex-wrap: wrap;
  gap: 0.5rem 1.5rem;
  padding: 1rem 1.5rem;
  background: var(--ink);
  color: var(--chalk);
}

.brand { font-size: 1.5rem; text-decoration: none; }
.top nav { display: flex; gap: 1.25rem; flex-wrap: wrap; }
.top nav a { text-decoration: none; }
.top nav a:hover { color: var(--orange); }

.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-wrap: wrap;
  gap: 3rem;
  padding: 5rem 1.5rem;
  background: var(--ink);
  color: var(--chalk);
}

.hero-text { max-width: 32rem; }

.hero h1 {
  margin: 0 0 1rem;
  font-size: clamp(3.2rem, 11vw, 6rem);
}

.hero p {
  margin: 0 0 2rem;
  font-size: 1.15rem;
  color: #d5dae1;
}

.btn {
  display: inline-block;
  padding: 0.7rem 1.8rem;
  background: var(--orange);
  color: var(--ink);
  font-size: 1.3rem;
  text-decoration: none;
  border-radius: 999px;
}

.btn:hover { background: var(--chalk); }

/* Ball drawn in CSS, no images */
.ball {
  position: relative;
  width: clamp(11rem, 30vw, 16rem);
  aspect-ratio: 1;
  border-radius: 50%;
  background: radial-gradient(circle at 35% 30%, #ff8a55, var(--orange) 55%, #c93d0d);
  overflow: hidden;
}

.ball::before,
.ball::after {
  content: "";
  position: absolute;
  background: var(--ink);
}

.ball::before { left: 50%; top: 0; bottom: 0; width: 4px; transform: translateX(-50%); }
.ball::after { top: 50%; left: 0; right: 0; height: 4px; transform: translateY(-50%); }

.block {
  max-width: 60rem;
  margin: 0 auto;
  padding: 4rem 1.5rem;
}

.block h2 { margin: 0 0 1.5rem; font-size: 2.5rem; }

.cols {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(16rem, 1fr));
  gap: 1.5rem;
}

.cols p { margin: 0; font-size: 1.1rem; }

.dark {
  max-width: none;
  background: var(--ink);
  color: var(--chalk);
}

.dark > * { max-width: 60rem; margin-left: auto; margin-right: auto; }

.list { padding: 0; list-style: none; display: grid; gap: 1rem; }
.list li { padding-left: 1rem; border-left: 4px solid var(--orange); font-size: 1.1rem; }

table { width: 100%; border-collapse: collapse; }
th, td { padding: 0.8rem 0; text-align: left; border-bottom: 1px solid var(--line); }
th { width: 40%; font-weight: 600; color: var(--steel); }

.center { text-align: center; }
.center p { margin: 0 0 1.5rem; font-size: 1.1rem; }

footer {
  padding: 1.5rem;
  background: var(--ink);
  color: var(--steel);
  text-align: center;
  font-size: 0.9rem;
}

footer p { margin: 0; }

@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
}
