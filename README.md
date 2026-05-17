<!DOCTYPE html>
<html lang="en">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Mohsin Syed Ali | AIML Professional Portfolio</title>
<link href="https://fonts.googleapis.com/css2?family=Playfair+Display:wght@400;700;900&family=DM+Sans:wght@300;400;500&family=Space+Mono:wght@400;700&display=swap" rel="stylesheet">
<style>
  :root {
    --crimson: #8B0000;
    --gold: #C9A84C;
    --cream: #FAF7F2;
    --charcoal: #1A1A1A;
    --slate: #3D3D3D;
    --light-gray: #EFEFEF;
    --white: #FFFFFF;
    --accent: #D4A853;
    --navy: #0A1628;
    --teal: #0E7490;
    --cyan: #06B6D4;
    --mint: #34D399;
    --deep: #0D2240;
    --card-bg: #132035;
  }

  * { margin: 0; padding: 0; box-sizing: border-box; }

  body {
    font-family: 'DM Sans', sans-serif;
    background: var(--cream);
    color: var(--charcoal);
    line-height: 1.7;
  }

  /* ── NAV ─────────────────────────────────────────────── */
  nav {
    position: fixed; top: 0; left: 0; right: 0; z-index: 100;
    background: rgba(139,0,0,0.97);
    backdrop-filter: blur(10px);
    display: flex; justify-content: space-between; align-items: center;
    padding: 1rem 3rem;
    border-bottom: 2px solid var(--gold);
  }
  .nav-brand {
    font-family: 'Space Mono', monospace;
    color: var(--gold);
    font-size: 0.85rem;
    letter-spacing: 0.15em;
    text-transform: uppercase;
  }
  .nav-links { display: flex; gap: 2rem; list-style: none; }
  .nav-links a {
    color: var(--cream);
    text-decoration: none;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    transition: color 0.2s;
  }
  .nav-links a:hover { color: var(--gold); }

  /* ── HERO ────────────────────────────────────────────── */
  .hero {
    min-height: 100vh;
    background: linear-gradient(135deg, var(--crimson) 0%, #4A0000 60%, #1A0000 100%);
    display: flex; align-items: center;
    padding: 8rem 3rem 4rem;
    position: relative;
    overflow: hidden;
  }
  .hero::before {
    content: '';
    position: absolute; inset: 0;
    background-image: radial-gradient(circle at 80% 20%, rgba(201,168,76,0.15) 0%, transparent 50%),
                      radial-gradient(circle at 20% 80%, rgba(201,168,76,0.08) 0%, transparent 40%);
  }
  .hero::after {
    content: 'AI/ML';
    position: absolute;
    right: -2rem; bottom: -3rem;
    font-family: 'Playfair Display', serif;
    font-size: 18rem;
    font-weight: 900;
    color: rgba(255,255,255,0.03);
    letter-spacing: -0.05em;
    line-height: 1;
    pointer-events: none;
  }
  .hero-content { position: relative; max-width: 900px; }
  .hero-tag {
    display: inline-block;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    letter-spacing: 0.2em;
    text-transform: uppercase;
    color: var(--gold);
    border: 1px solid var(--gold);
    padding: 0.4rem 1rem;
    margin-bottom: 2rem;
  }
  .hero h1 {
    font-family: 'Playfair Display', serif;
    font-size: clamp(3rem, 7vw, 6rem);
    font-weight: 900;
    color: var(--white);
    line-height: 1.05;
    margin-bottom: 1.5rem;
  }
  .hero h1 span { color: var(--gold); }
  .hero-sub {
    font-size: 1.1rem;
    color: rgba(255,255,255,0.75);
    max-width: 560px;
    margin-bottom: 3rem;
    font-weight: 300;
  }
  .hero-ctas { display: flex; gap: 1rem; flex-wrap: wrap; }
  .hero-cta {
    display: inline-block;
    background: var(--gold);
    color: var(--charcoal);
    padding: 0.9rem 2.5rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.8rem;
    letter-spacing: 0.1em;
    text-transform: uppercase;
    text-decoration: none;
    font-weight: 700;
    transition: all 0.2s;
  }
  .hero-cta:hover { background: var(--white); transform: translateY(-2px); }
  .hero-cta.secondary {
    background: transparent;
    color: var(--gold);
    border: 1px solid var(--gold);
  }
  .hero-cta.secondary:hover { background: var(--gold); color: var(--charcoal); }

  /* Artifact badge counter in hero */
  .hero-artifacts {
    display: flex; gap: 1.5rem; margin-top: 2rem; flex-wrap: wrap;
  }
  .hero-artifact-badge {
    display: flex; align-items: center; gap: 0.6rem;
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    color: rgba(255,255,255,0.6);
    letter-spacing: 0.08em;
  }
  .badge-dot {
    width: 8px; height: 8px; border-radius: 50%;
  }
  .badge-dot.art1 { background: var(--gold); }
  .badge-dot.art2 { background: var(--mint); }

  /* ── SECTIONS ────────────────────────────────────────── */
  section { padding: 5rem 3rem; }
  .section-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem;
    letter-spacing: 0.25em;
    text-transform: uppercase;
    color: var(--crimson);
    margin-bottom: 0.75rem;
  }
  .section-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 700;
    color: var(--charcoal);
    margin-bottom: 2rem;
  }
  .section-title span { color: var(--crimson); }
  .divider { width: 60px; height: 3px; background: var(--gold); margin-bottom: 2.5rem; }

  /* ── BIO ─────────────────────────────────────────────── */
  .bio-section { background: var(--white); }
  .bio-grid { display: grid; grid-template-columns: 1fr 1fr; gap: 4rem; align-items: start; max-width: 1100px; margin: 0 auto; }
  .bio-text p { color: var(--slate); margin-bottom: 1rem; font-size: 1rem; }
  .bio-stats { display: grid; grid-template-columns: 1fr 1fr; gap: 1.5rem; }
  .stat-card {
    background: var(--cream);
    border-left: 4px solid var(--crimson);
    padding: 1.5rem;
  }
  .stat-num { font-family: 'Playfair Display', serif; font-size: 2.5rem; font-weight: 900; color: var(--crimson); line-height: 1; }
  .stat-label { font-size: 0.8rem; color: var(--slate); margin-top: 0.3rem; text-transform: uppercase; letter-spacing: 0.08em; }

  /* ── VALUE PROPOSITION ───────────────────────────────── */
  .vp-section { background: var(--charcoal); }
  .vp-section .section-label { color: var(--gold); }
  .vp-section .section-title { color: var(--white); }
  .vp-card {
    background: rgba(255,255,255,0.05);
    border: 1px solid rgba(201,168,76,0.3);
    border-left: 5px solid var(--gold);
    padding: 2.5rem;
    max-width: 800px;
    font-family: 'Playfair Display', serif;
    font-size: 1.3rem;
    color: var(--cream);
    font-style: italic;
    line-height: 1.8;
    margin-bottom: 2rem;
  }
  .vp-pillars { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1.5rem; max-width: 1000px; }
  .vp-pillar { background: rgba(255,255,255,0.04); border-top: 3px solid var(--gold); padding: 1.5rem; }
  .vp-pillar-title { font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--gold); letter-spacing: 0.1em; margin-bottom: 0.5rem; }
  .vp-pillar p { font-size: 0.85rem; color: rgba(255,255,255,0.65); }

  /* ── PORTFOLIO OVERVIEW ──────────────────────────────── */
  .portfolio-overview {
    background: var(--cream);
    padding: 5rem 3rem;
  }
  .portfolio-overview .section-label { color: var(--crimson); }
  .artifacts-index {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2rem;
    max-width: 1100px;
    margin-top: 0;
  }
  .artifact-index-card {
    background: var(--white);
    border-top: 5px solid var(--gold);
    padding: 2rem;
    display: flex;
    flex-direction: column;
    gap: 1rem;
    transition: transform 0.2s, box-shadow 0.2s;
    cursor: pointer;
    text-decoration: none;
    color: inherit;
  }
  .artifact-index-card:hover { transform: translateY(-4px); box-shadow: 0 12px 30px rgba(0,0,0,0.1); }
  .artifact-index-card.art2 { border-top-color: var(--teal); }
  .aic-num {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem;
    letter-spacing: 0.2em;
    color: var(--crimson);
    text-transform: uppercase;
  }
  .artifact-index-card.art2 .aic-num { color: var(--teal); }
  .aic-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.4rem;
    font-weight: 700;
    color: var(--charcoal);
    line-height: 1.3;
  }
  .aic-desc { font-size: 0.9rem; color: var(--slate); }
  .aic-tags { display: flex; flex-wrap: wrap; gap: 0.5rem; }
  .aic-tag {
    font-family: 'Space Mono', monospace;
    font-size: 0.6rem;
    padding: 0.25rem 0.6rem;
    letter-spacing: 0.08em;
    text-transform: uppercase;
    background: var(--cream);
    color: var(--crimson);
    border: 1px solid rgba(139,0,0,0.2);
  }
  .artifact-index-card.art2 .aic-tag { color: var(--teal); border-color: rgba(14,116,144,0.3); }
  .aic-arrow {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem;
    color: var(--gold);
    letter-spacing: 0.1em;
    margin-top: auto;
  }

  /* ── ARTIFACT 1 ──────────────────────────────────────── */
  .artifact-section { background: var(--cream); }
  .artifact-meta {
    display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem;
    max-width: 1100px; margin-bottom: 3rem;
  }
  .meta-card { background: var(--white); border-top: 3px solid var(--crimson); padding: 1.5rem; }
  .meta-card h4 { font-family: 'Space Mono', monospace; font-size: 0.7rem; color: var(--crimson); letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 0.5rem; }
  .meta-card p { font-size: 0.9rem; color: var(--slate); }

  .infographic { max-width: 1100px; margin: 0 auto; }
  .infographic-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.6rem;
    color: var(--charcoal);
    border-bottom: 2px solid var(--crimson);
    padding-bottom: 0.75rem;
    margin-bottom: 2rem;
  }
  .domains-row { display: grid; grid-template-columns: 200px repeat(4, 1fr); gap: 2px; margin-bottom: 2px; }
  .domain-header {
    background: var(--crimson); color: var(--white);
    font-family: 'Space Mono', monospace; font-size: 0.7rem;
    letter-spacing: 0.1em; text-transform: uppercase;
    padding: 0.75rem 1rem; text-align: center; font-weight: 700;
  }
  .domain-header:first-child { background: var(--charcoal); }
  .algo-row { display: grid; grid-template-columns: 200px repeat(4, 1fr); gap: 2px; margin-bottom: 2px; }
  .algo-name {
    background: var(--white); border-left: 4px solid var(--crimson);
    padding: 1rem; display: flex; flex-direction: column; justify-content: center;
  }
  .algo-name strong { font-size: 0.85rem; color: var(--charcoal); display: block; margin-bottom: 0.2rem; }
  .algo-name .algo-type { font-family: 'Space Mono', monospace; font-size: 0.62rem; color: var(--crimson); letter-spacing: 0.05em; text-transform: uppercase; }
  .algo-cell {
    background: var(--light-gray); padding: 0.75rem 0.5rem; text-align: center;
    font-size: 0.78rem; color: var(--slate);
    display: flex; align-items: center; justify-content: center;
    min-height: 70px; line-height: 1.4;
  }
  .algo-cell.active { background: linear-gradient(135deg,#fff8ee,#fef0d5); border: 1px solid var(--gold); color: var(--charcoal); font-weight: 500; }
  .algo-cell.primary { background: linear-gradient(135deg,#fff0f0,#ffe0e0); border: 1px solid var(--crimson); color: var(--crimson); font-weight: 600; }
  .legend { display: flex; gap: 2rem; margin-top: 1.5rem; flex-wrap: wrap; }
  .legend-item { display: flex; align-items: center; gap: 0.5rem; font-size: 0.8rem; color: var(--slate); }
  .legend-box { width: 20px; height: 14px; }
  .legend-box.primary { background: #ffe0e0; border: 1px solid var(--crimson); }
  .legend-box.active { background: #fff8ee; border: 1px solid var(--gold); }
  .legend-box.inactive { background: var(--light-gray); }
  .algo-cards { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; margin-top: 3rem; max-width: 1100px; }
  .algo-card { background: var(--white); border-top: 4px solid var(--gold); padding: 1.5rem; }
  .algo-card-header { display: flex; align-items: flex-start; justify-content: space-between; margin-bottom: 0.75rem; }
  .algo-card h3 { font-family: 'Playfair Display', serif; font-size: 1.1rem; color: var(--charcoal); }
  .tag { display: inline-block; font-family: 'Space Mono', monospace; font-size: 0.6rem; padding: 0.2rem 0.6rem; letter-spacing: 0.08em; text-transform: uppercase; border-radius: 2px; }
  .tag.supervised { background: #ffe0e0; color: var(--crimson); }
  .tag.unsupervised { background: #e0eaff; color: #1a3a7a; }
  .tag.both { background: #e8ffe0; color: #1a6a1a; }
  .algo-card p { font-size: 0.85rem; color: var(--slate); margin-bottom: 0.75rem; }
  .use-case { font-size: 0.78rem; color: var(--charcoal); background: var(--cream); padding: 0.5rem 0.75rem; border-left: 3px solid var(--gold); }
  .use-case strong { color: var(--crimson); }

  /* ── ARTIFACT 2 — NEURAL NETWORKS ────────────────────── */
  .artifact2-section {
    background: var(--navy);
    padding: 5rem 3rem;
  }
  .artifact2-section .section-label { color: var(--mint); }
  .artifact2-inner { max-width: 1100px; margin: 0 auto; }

  /* Header */
  .a2-title {
    font-family: 'Playfair Display', serif;
    font-size: clamp(2rem, 4vw, 3rem);
    font-weight: 700;
    color: var(--white);
    margin-bottom: 2rem;
  }
  .a2-title span { color: var(--cyan); }
  .divider-teal { width: 60px; height: 3px; background: var(--teal); margin-bottom: 2.5rem; }

  /* Meta cards */
  .a2-meta { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-bottom: 3.5rem; }
  .a2-meta-card {
    background: var(--deep);
    border-top: 3px solid var(--teal);
    padding: 1.5rem;
  }
  .a2-meta-card h4 {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem; color: var(--cyan);
    letter-spacing: 0.15em; text-transform: uppercase; margin-bottom: 0.5rem;
  }
  .a2-meta-card p { font-size: 0.9rem; color: rgba(255,255,255,0.65); }

  /* Component grid */
  .a2-components-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem; letter-spacing: 0.2em;
    color: var(--teal); text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .a2-components { display: grid; grid-template-columns: repeat(3, 1fr); gap: 1.5rem; margin-bottom: 3.5rem; }
  .a2-comp-card {
    background: var(--deep);
    border: 1px solid rgba(14,116,144,0.4);
    border-top: 3px solid var(--teal);
    padding: 1.75rem;
  }
  .a2-comp-card.highlight { border-top-color: var(--mint); border-color: rgba(52,211,153,0.3); }
  .a2-comp-card.highlight2 { border-top-color: var(--cyan); border-color: rgba(6,182,212,0.3); }
  .comp-icon {
    font-size: 1.6rem;
    margin-bottom: 0.75rem;
    display: block;
  }
  .comp-name {
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem; letter-spacing: 0.12em;
    color: var(--mint); text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  .a2-comp-card.highlight2 .comp-name { color: var(--cyan); }
  .a2-comp-card:not(.highlight):not(.highlight2) .comp-name { color: rgba(255,255,255,0.5); }
  .comp-title {
    font-family: 'Playfair Display', serif;
    font-size: 1.2rem; font-weight: 700;
    color: var(--white); margin-bottom: 0.75rem;
  }
  .comp-desc { font-size: 0.88rem; color: rgba(255,255,255,0.65); line-height: 1.6; margin-bottom: 1rem; }
  .comp-example {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem;
    color: var(--cyan);
    background: rgba(6,182,212,0.08);
    border: 1px solid rgba(6,182,212,0.2);
    padding: 0.5rem 0.75rem;
    line-height: 1.6;
  }

  /* Architecture diagram */
  .a2-diagram-wrap {
    background: var(--deep);
    border: 1px solid rgba(14,116,144,0.3);
    padding: 2.5rem;
    margin-bottom: 3.5rem;
  }
  .a2-diagram-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem; letter-spacing: 0.2em;
    color: var(--teal); text-transform: uppercase;
    margin-bottom: 2rem;
  }
  /* SVG network diagram */
  .nn-diagram {
    width: 100%;
    max-width: 960px;
    display: block;
    margin: 0 auto;
  }

  /* Training loop */
  .a2-loop-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem; letter-spacing: 0.2em;
    color: var(--teal); text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .a2-training-loop { display: grid; grid-template-columns: repeat(5, 1fr); gap: 0; margin-bottom: 1.5rem; }
  .loop-step { position: relative; }
  .loop-step-inner {
    background: var(--card-bg);
    border: 1px solid rgba(14,116,144,0.3);
    padding: 1.25rem 1rem;
    height: 100%;
    display: flex; flex-direction: column; align-items: center; text-align: center; gap: 0.5rem;
  }
  .loop-num {
    width: 36px; height: 36px; border-radius: 50%;
    display: flex; align-items: center; justify-content: center;
    font-family: 'Space Mono', monospace;
    font-weight: 700; font-size: 0.9rem;
    color: var(--navy);
    flex-shrink: 0;
  }
  .loop-step:nth-child(1) .loop-num { background: var(--mint); }
  .loop-step:nth-child(2) .loop-num { background: var(--cyan); }
  .loop-step:nth-child(3) .loop-num { background: #F59E0B; }
  .loop-step:nth-child(4) .loop-num { background: #F97316; }
  .loop-step:nth-child(5) .loop-num { background: #EF4444; }
  .loop-step-name {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem; letter-spacing: 0.08em;
    text-transform: uppercase;
    font-weight: 700;
  }
  .loop-step:nth-child(1) .loop-step-name { color: var(--mint); }
  .loop-step:nth-child(2) .loop-step-name { color: var(--cyan); }
  .loop-step:nth-child(3) .loop-step-name { color: #F59E0B; }
  .loop-step:nth-child(4) .loop-step-name { color: #F97316; }
  .loop-step:nth-child(5) .loop-step-name { color: #EF4444; }
  .loop-step-desc { font-size: 0.78rem; color: rgba(255,255,255,0.55); line-height: 1.5; }
  .loop-arrow {
    position: absolute; right: -1px; top: 50%;
    transform: translateY(-50%);
    z-index: 2;
    font-size: 0.8rem; color: var(--teal);
    background: var(--navy);
    padding: 0 2px;
  }
  .loop-repeat {
    background: var(--card-bg);
    border: 1px solid var(--teal);
    padding: 0.65rem 1.5rem;
    text-align: center;
    font-family: 'Space Mono', monospace;
    font-size: 0.75rem; letter-spacing: 0.1em;
    color: var(--cyan);
    margin-bottom: 3.5rem;
  }

  /* Summary insights */
  .a2-summary-title {
    font-family: 'Space Mono', monospace;
    font-size: 0.7rem; letter-spacing: 0.2em;
    color: var(--teal); text-transform: uppercase;
    margin-bottom: 1.5rem;
  }
  .a2-insights { display: grid; grid-template-columns: repeat(2, 1fr); gap: 1.5rem; margin-bottom: 2.5rem; }
  .a2-insight {
    background: var(--card-bg);
    border: 1px solid rgba(14,116,144,0.3);
    border-left: 4px solid var(--teal);
    padding: 1.5rem;
  }
  .a2-insight h4 {
    font-family: 'Space Mono', monospace;
    font-size: 0.72rem; letter-spacing: 0.08em;
    color: var(--mint); text-transform: uppercase;
    margin-bottom: 0.5rem;
  }
  .a2-insight p { font-size: 0.88rem; color: rgba(255,255,255,0.65); }

  /* Download note */
  .a2-download {
    background: rgba(14,116,144,0.1);
    border: 1px solid rgba(14,116,144,0.4);
    padding: 1.25rem 1.75rem;
    display: flex; align-items: center; gap: 1.25rem;
    flex-wrap: wrap;
  }
  .a2-download p { font-size: 0.9rem; color: rgba(255,255,255,0.7); flex: 1; }
  .a2-download p strong { color: var(--white); }
  .a2-dl-label {
    font-family: 'Space Mono', monospace;
    font-size: 0.65rem; letter-spacing: 0.15em;
    text-transform: uppercase; color: var(--cyan);
    white-space: nowrap;
    border: 1px solid var(--cyan);
    padding: 0.4rem 1rem;
  }

  /* ── PROCESS ─────────────────────────────────────────── */
  .process-section { background: var(--white); }
  .process-steps { display: grid; grid-template-columns: repeat(4, 1fr); gap: 1px; background: var(--light-gray); max-width: 1100px; }
  .process-step { background: var(--white); padding: 2rem 1.5rem; }
  .step-num { font-family: 'Playfair Display', serif; font-size: 3rem; font-weight: 900; color: rgba(139,0,0,0.08); line-height: 1; margin-bottom: 0.5rem; }
  .step-title { font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--crimson); letter-spacing: 0.1em; text-transform: uppercase; margin-bottom: 0.5rem; }
  .process-step p { font-size: 0.85rem; color: var(--slate); }

  /* ── TOOLS ───────────────────────────────────────────── */
  .tools-section { background: var(--cream); }
  .tools-grid { display: flex; flex-wrap: wrap; gap: 1rem; max-width: 900px; }
  .tool-chip { background: var(--white); border: 1px solid rgba(139,0,0,0.2); padding: 0.5rem 1.2rem; font-family: 'Space Mono', monospace; font-size: 0.75rem; color: var(--charcoal); letter-spacing: 0.05em; }
  .tool-chip:hover { background: var(--crimson); color: var(--white); }

  /* ── FOOTER ──────────────────────────────────────────── */
  footer {
    background: var(--charcoal);
    color: rgba(255,255,255,0.5);
    padding: 3rem;
    text-align: center;
    font-size: 0.8rem;
    font-family: 'Space Mono', monospace;
    letter-spacing: 0.05em;
  }
  footer span { color: var(--gold); }
  .footer-artifacts {
    display: flex; justify-content: center; gap: 2rem;
    margin-top: 1.5rem; flex-wrap: wrap;
  }
  .footer-artifact {
    font-size: 0.7rem; color: rgba(255,255,255,0.35);
    border-top: 2px solid var(--gold); padding-top: 0.5rem;
    max-width: 220px; text-align: left;
  }
  .footer-artifact.art2 { border-top-color: var(--teal); }
  .footer-artifact strong { display: block; color: rgba(255,255,255,0.6); margin-bottom: 0.2rem; }

  /* ── RESPONSIVE ──────────────────────────────────────── */
  @media (max-width: 900px) {
    nav { padding: 1rem 1.5rem; }
    .nav-links { display: none; }
    section, .artifact2-section, .portfolio-overview { padding: 3.5rem 1.5rem; }
    .bio-grid { grid-template-columns: 1fr; gap: 2rem; }
    .vp-pillars { grid-template-columns: repeat(2, 1fr); }
    .artifact-meta, .a2-meta { grid-template-columns: 1fr; }
    .domains-row, .algo-row { grid-template-columns: 130px repeat(4, 1fr); font-size: 0.68rem; }
    .algo-cards { grid-template-columns: 1fr; }
    .process-steps { grid-template-columns: repeat(2, 1fr); }
    .artifacts-index { grid-template-columns: 1fr; }
    .a2-components { grid-template-columns: 1fr 1fr; }
    .a2-training-loop { grid-template-columns: 1fr; }
    .loop-arrow { display: none; }
    .a2-insights { grid-template-columns: 1fr; }
  }
  @media (max-width: 600px) {
    .a2-components { grid-template-columns: 1fr; }
  }

  /* ── ANIMATIONS ──────────────────────────────────────── */
  @keyframes fadeUp {
    from { opacity: 0; transform: translateY(30px); }
    to   { opacity: 1; transform: translateY(0); }
  }
  .hero-tag  { animation: fadeUp 0.6s ease both; }
  .hero h1   { animation: fadeUp 0.6s 0.15s ease both; }
  .hero-sub  { animation: fadeUp 0.6s 0.3s  ease both; }
  .hero-ctas { animation: fadeUp 0.6s 0.45s ease both; }
  .hero-artifacts { animation: fadeUp 0.6s 0.6s ease both; }

  /* Section divider between artifacts */
  .artifact-divider {
    height: 4px;
    background: linear-gradient(90deg, var(--crimson), var(--gold), var(--teal), var(--cyan));
  }
</style>
</head>
<body>

<!-- NAV -->
<nav>
  <div class="nav-brand">Mohsin Syed Ali · AIML Portfolio</div>
  <ul class="nav-links">
    <li><a href="#bio">About</a></li>
    <li><a href="#vp">Value Proposition</a></li>
    <li><a href="#artifact1">Artifact 1</a></li>
    <li><a href="#artifact2">Artifact 2</a></li>
    <li><a href="#process">Process</a></li>
  </ul>
</nav>

<!-- HERO -->
<section class="hero">
  <div class="hero-content">
    <div class="hero-tag">AIML Professional Portfolio · Indiana Wesleyan University</div>
    <h1>Mohsin<br>Syed <span>Ali</span></h1>
    <p class="hero-sub">Emerging AI & Machine Learning practitioner building expertise in intelligent systems, data-driven decision-making, and generative AI applications.</p>
    <div class="hero-ctas">
      <a href="#artifact1" class="hero-cta">Artifact 1: ML Algorithms →</a>
      <a href="#artifact2" class="hero-cta secondary">Artifact 2: Neural Networks →</a>
    </div>
    <div class="hero-artifacts">
      <div class="hero-artifact-badge"><span class="badge-dot art1"></span> ML Algorithm Visual Framework</div>
      <div class="hero-artifact-badge"><span class="badge-dot art2"></span> Neural Networks: Structure & Components</div>
    </div>
  </div>
</section>

<!-- BIO -->
<section class="bio-section" id="bio">
  <div class="bio-grid">
    <div class="bio-text">
      <div class="section-label">Professional Bio</div>
      <div class="section-title">About <span>Me</span></div>
      <div class="divider"></div>
      <p>My name is Mohsin Syed Ali, and I am an AIML student at Indiana Wesleyan University with a growing passion for the intersection of data science, machine learning, and real-world problem solving.</p>
      <p>My journey into AI and machine learning is driven by curiosity — a desire to understand not just how algorithms work, but how they can be applied to create meaningful outcomes for organizations and individuals. I bring a structured, analytical approach to problem-solving combined with a commitment to continuous learning in this rapidly evolving field.</p>
      <p>Through my coursework, I am building competencies across supervised and unsupervised learning, computer vision, natural language processing, and generative AI — areas that represent the cutting edge of technological innovation. My goal is to leverage these skills to help organizations make smarter, data-informed decisions.</p>
    </div>
    <div>
      <div class="bio-stats">
        <div class="stat-card"><div class="stat-num">10+</div><div class="stat-label">ML Algorithms Studied</div></div>
        <div class="stat-card"><div class="stat-num">4</div><div class="stat-label">AI Domains Explored</div></div>
        <div class="stat-card"><div class="stat-num">2</div><div class="stat-label">Portfolio Artifacts</div></div>
        <div class="stat-card"><div class="stat-num">IWU</div><div class="stat-label">Indiana Wesleyan University</div></div>
      </div>
    </div>
  </div>
</section>

<!-- VALUE PROPOSITION -->
<section class="vp-section" id="vp">
  <div class="section-label">Personal Value Proposition</div>
  <div class="section-title" style="color:var(--white);">What I <span style="color:var(--gold);">Bring</span></div>
  <div class="divider"></div>
  <div class="vp-card">
    "As an AI/ML student with a foundational background in machine learning algorithms, data pattern recognition, and generative AI concepts, I help organizations and peers bridge the gap between theoretical AI knowledge and practical application — translating complex algorithmic frameworks into clear, actionable insights that support smarter decision-making and innovation."
  </div>
  <div class="vp-pillars">
    <div class="vp-pillar"><div class="vp-pillar-title">Clarity</div><p>I translate complex ML concepts into accessible frameworks anyone can understand.</p></div>
    <div class="vp-pillar"><div class="vp-pillar-title">Focus</div><p>Grounded in practical, real-world application of AI/ML across key industry domains.</p></div>
    <div class="vp-pillar"><div class="vp-pillar-title">Growth</div><p>Actively developing skills at the forefront of AI, including generative AI systems.</p></div>
    <div class="vp-pillar"><div class="vp-pillar-title">Impact</div><p>Committed to using AI knowledge to drive meaningful outcomes for organizations.</p></div>
  </div>
</section>

<!-- PORTFOLIO OVERVIEW -->
<section class="portfolio-overview" id="portfolio">
  <div class="section-label">Portfolio Artifacts</div>
  <div class="section-title">Work <span>Samples</span></div>
  <div class="divider"></div>
  <div class="artifacts-index">
    <a href="#artifact1" class="artifact-index-card">
      <div class="aic-num">Artifact 01 · ML Algorithms</div>
      <div class="aic-title">Machine Learning Algorithm Visual Framework</div>
      <div class="aic-desc">A comparative matrix mapping 10 key ML algorithms across four domains: Tabular Data, Computer Vision, NLP, and Generative AI — with real-world use cases for each.</div>
      <div class="aic-tags">
        <span class="aic-tag">Supervised Learning</span>
        <span class="aic-tag">Unsupervised Learning</span>
        <span class="aic-tag">Generative AI</span>
        <span class="aic-tag">Visual Framework</span>
      </div>
      <div class="aic-arrow">View Artifact →</div>
    </a>
    <a href="#artifact2" class="artifact-index-card art2">
      <div class="aic-num">Artifact 02 · Neural Networks</div>
      <div class="aic-title">Neural Networks: Structure &amp; Components</div>
      <div class="aic-desc">An in-depth visual breakdown of all six core neural network components — Layers, Neurons, Weights, Activation Functions, Loss Functions, and Optimization Algorithms — with an interactive architecture diagram and training loop flowchart.</div>
      <div class="aic-tags">
        <span class="aic-tag">Deep Learning</span>
        <span class="aic-tag">Neural Architecture</span>
        <span class="aic-tag">Backpropagation</span>
        <span class="aic-tag">TF Playground</span>
      </div>
      <div class="aic-arrow">View Artifact →</div>
    </a>
  </div>
</section>

<div class="artifact-divider"></div>

<!-- ════════════════════════════════════════════════════════
     ARTIFACT 1 — ML ALGORITHM VISUAL FRAMEWORK
     ════════════════════════════════════════════════════════ -->
<section class="artifact-section" id="artifact1">
  <div class="section-label">Portfolio Artifact · 01</div>
  <div class="section-title">ML Algorithm <span>Visual Framework</span></div>
  <div class="divider"></div>

  <div class="artifact-meta">
    <div class="meta-card">
      <h4>Objective</h4>
      <p>To categorize and visually map 10 key machine learning algorithms across their learning types and primary application domains including Tabular Data, Computer Vision, NLP, and Generative AI.</p>
    </div>
    <div class="meta-card">
      <h4>Tools Used</h4>
      <p>Research synthesis · Visual framework design · Comparative matrix · Real-world use case analysis · Portfolio documentation</p>
    </div>
    <div class="meta-card">
      <h4>Artifact Value</h4>
      <p>This framework serves as a quick-reference guide for practitioners selecting appropriate ML algorithms — demonstrating my ability to synthesize and communicate complex AI concepts clearly.</p>
    </div>
  </div>

  <div class="infographic">
    <div class="infographic-title">Machine Learning Algorithm Domain Matrix</div>
    <div class="domains-row">
      <div class="domain-header">Algorithm</div>
      <div class="domain-header">📊 Tabular Data</div>
      <div class="domain-header">🖼 Computer Vision</div>
      <div class="domain-header">💬 NLP</div>
      <div class="domain-header">✨ Generative AI</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Random Forest</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Classification &amp; Regression<br>on structured data</div>
      <div class="algo-cell active">Basic image classification</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Gradient Boosting (XGBoost)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">High-accuracy prediction;<br>Kaggle competitions</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Decision Tree</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Rule-based classification;<br>Loan approval</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Support Vector Machine</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell active">High-dimensional classification</div>
      <div class="algo-cell active">Image classification (small data)</div>
      <div class="algo-cell active">Text classification</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Linear Regression</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell primary">Price prediction;<br>Trend forecasting</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>CNN (Convolutional NN)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Image classification;<br>Object detection; Face ID</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">Image generation base layer</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Transformer (GPT/BERT)</strong><span class="algo-type">Supervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Language modeling;<br>Sentiment analysis; QA</div>
      <div class="algo-cell primary">Text generation;<br>ChatGPT, Claude</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>K-Means Clustering</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell primary">Customer segmentation;<br>Anomaly detection</div>
      <div class="algo-cell active">Image segmentation</div>
      <div class="algo-cell active">Topic clustering</div>
      <div class="algo-cell">—</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>GAN (Generative Adversarial)</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">Synthetic image creation</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Image generation;<br>Deepfakes; Art synthesis</div>
    </div>
    <div class="algo-row">
      <div class="algo-name"><strong>Diffusion Model</strong><span class="algo-type">Unsupervised</span></div>
      <div class="algo-cell">—</div>
      <div class="algo-cell active">High-fidelity image synthesis</div>
      <div class="algo-cell">—</div>
      <div class="algo-cell primary">Text-to-image generation;<br>DALL·E, Midjourney</div>
    </div>
    <div class="legend">
      <div class="legend-item"><div class="legend-box primary"></div> Primary domain application</div>
      <div class="legend-item"><div class="legend-box active"></div> Secondary / supporting use</div>
      <div class="legend-item"><div class="legend-box inactive"></div> Not applicable</div>
    </div>
  </div>

  <div class="algo-cards">
    <div class="algo-card">
      <div class="algo-card-header"><h3>Random Forest</h3><span class="tag supervised">Supervised</span></div>
      <p>An ensemble method that builds multiple decision trees during training and merges them for more accurate, stable predictions. It reduces overfitting through randomness in feature selection.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Credit risk scoring, medical diagnosis, fraud detection in financial transactions.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>Gradient Boosting (XGBoost)</h3><span class="tag supervised">Supervised</span></div>
      <p>Builds trees sequentially, where each new tree corrects errors of the previous ones. Known for exceptional performance on tabular/structured datasets.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Competitive ML benchmarks, click-through rate prediction, e-commerce recommendation ranking.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>Decision Tree</h3><span class="tag supervised">Supervised</span></div>
      <p>A flowchart-like model that splits data based on feature values. Highly interpretable and ideal for rule-based classification tasks where transparency matters.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Loan approval decisions, medical triage, customer churn classification.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>Support Vector Machine (SVM)</h3><span class="tag supervised">Supervised</span></div>
      <p>Finds the optimal hyperplane that best separates data classes with maximum margin. Effective in high-dimensional spaces and works well for text classification tasks.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Email spam filtering, image categorization, bioinformatics gene classification.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>CNN (Convolutional Neural Network)</h3><span class="tag supervised">Supervised</span></div>
      <p>Uses layers of convolutional filters to automatically learn spatial hierarchies of features from images. The go-to architecture for all visual recognition tasks.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Face recognition (Face ID), tumor detection in medical imaging, autonomous vehicle object detection.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>Transformer (GPT / BERT)</h3><span class="tag supervised">Supervised</span></div>
      <p>Uses self-attention mechanisms to model relationships between all words in a sequence simultaneously, enabling context-aware language understanding at massive scale.</p>
      <div class="use-case"><strong>Real-World Use:</strong> ChatGPT, Google Search, sentiment analysis, legal document summarization.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>K-Means Clustering</h3><span class="tag unsupervised">Unsupervised</span></div>
      <p>Groups data into K clusters by iteratively assigning points to the nearest centroid and updating centroids. No labels required — discovers natural structure in data.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Customer segmentation for marketing, document clustering, anomaly detection in network security.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>GAN (Generative Adversarial Network)</h3><span class="tag unsupervised">Unsupervised</span></div>
      <p>Two networks compete — a generator creates synthetic data and a discriminator judges authenticity. This adversarial process produces highly realistic synthetic outputs.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Synthetic training data generation, deepfake creation, photo enhancement, drug molecule generation.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>Diffusion Model</h3><span class="tag unsupervised">Unsupervised</span></div>
      <p>Learns to reverse a gradual noising process — starting from pure noise and progressively denoising to generate a realistic image guided by text prompts.</p>
      <div class="use-case"><strong>Real-World Use:</strong> DALL·E 3, Stable Diffusion, Midjourney — text-to-image generation, AI art, creative design tools.</div>
    </div>
    <div class="algo-card">
      <div class="algo-card-header"><h3>PCA (Principal Component Analysis)</h3><span class="tag unsupervised">Unsupervised</span></div>
      <p>Reduces data dimensionality by finding principal components — directions of maximum variance. Used for visualization and as preprocessing for other algorithms.</p>
      <div class="use-case"><strong>Real-World Use:</strong> Gene expression analysis, image compression, exploratory data analysis, noise reduction.</div>
    </div>
  </div>
</section>

<div class="artifact-divider"></div>

<!-- ════════════════════════════════════════════════════════
     ARTIFACT 2 — NEURAL NETWORKS
     ════════════════════════════════════════════════════════ -->
<section class="artifact2-section" id="artifact2">
  <div class="artifact2-inner">

    <div class="section-label">Portfolio Artifact · 02</div>
    <div class="a2-title">Neural Networks: <span>Structure &amp; Components</span></div>
    <div class="divider-teal"></div>

    <!-- Meta -->
    <div class="a2-meta">
      <div class="a2-meta-card">
        <h4>Objective</h4>
        <p>Define and visually illustrate the six core components of a neural network — Layers, Neurons, Weights, Activation Functions, Loss Functions, and Optimization Algorithms — with diagrams and real-world context.</p>
      </div>
      <div class="a2-meta-card">
        <h4>Exploration</h4>
        <p>Hands-on experimentation using the TensorFlow Neural Network Playground — testing dataset types, noise levels, feature combinations, and neuron layers to observe their impact on model performance.</p>
      </div>
      <div class="a2-meta-card">
        <h4>Artifact Value</h4>
        <p>This artifact demonstrates deep learning literacy: the ability to deconstruct neural network internals, explain them visually, and connect theory to practice through the training loop.</p>
      </div>
    </div>

    <!-- ── COMPONENTS ───────────────────────────────── -->
    <div class="a2-components-title">▸ Six Core Neural Network Components</div>
    <div class="a2-components">

      <div class="a2-comp-card highlight">
        <span class="comp-icon">🧱</span>
        <div class="comp-name">Component 01</div>
        <div class="comp-title">Layers</div>
        <div class="comp-desc">Organized groups of neurons that process information in sequence. Every neural network has three layer types: an <strong style="color:#fff">Input Layer</strong> that receives raw data, one or more <strong style="color:#fff">Hidden Layers</strong> that learn abstract representations, and an <strong style="color:#fff">Output Layer</strong> that produces the final prediction. More hidden layers create "deeper" networks with greater representational capacity.</div>
        <div class="comp-example">Input Layer → Hidden Layer(s) → Output Layer<br>More layers = greater abstraction capacity</div>
      </div>

      <div class="a2-comp-card highlight2">
        <span class="comp-icon">🔵</span>
        <div class="comp-name">Component 02</div>
        <div class="comp-title">Neurons</div>
        <div class="comp-desc">The fundamental computational unit of a neural network, loosely inspired by biological neurons. Each neuron receives weighted inputs from the previous layer, computes a weighted sum plus a bias term, then passes the result through an activation function. The output becomes input to every neuron in the next layer.</div>
        <div class="comp-example">z = Σ(weight × input) + bias<br>output = activation_function(z)</div>
      </div>

      <div class="a2-comp-card highlight">
        <span class="comp-icon">⚖️</span>
        <div class="comp-name">Component 03</div>
        <div class="comp-title">Weights</div>
        <div class="comp-desc">Numerical parameters assigned to every connection between neurons. Weights determine the strength and direction of each signal. They are initialized randomly and then refined through training — specifically via backpropagation — so the network progressively improves its predictions. Biases (per-neuron learnable constants) work alongside weights to shift activation thresholds.</div>
        <div class="comp-example">High weight → strong influence on next neuron<br>Negative weight → inhibits activation</div>
      </div>

      <div class="a2-comp-card highlight2">
        <span class="comp-icon">⚡</span>
        <div class="comp-name">Component 04</div>
        <div class="comp-title">Activation Functions</div>
        <div class="comp-desc">Mathematical functions applied after the weighted sum that introduce non-linearity into the network. Without them, stacking layers would be mathematically equivalent to a single layer. Common choices include <strong style="color:#fff">ReLU</strong> (default for hidden layers), <strong style="color:#fff">Sigmoid</strong> (binary output), <strong style="color:#fff">Tanh</strong> (centered output), and <strong style="color:#fff">Softmax</strong> (multi-class probability).</div>
        <div class="comp-example">ReLU: f(x) = max(0, x)<br>Sigmoid: f(x) = 1 / (1 + e⁻ˣ)<br>Tanh: f(x) = (eˣ – e⁻ˣ) / (eˣ + e⁻ˣ)</div>
      </div>

      <div class="a2-comp-card highlight">
        <span class="comp-icon">📉</span>
        <div class="comp-name">Component 05</div>
        <div class="comp-title">Loss Functions</div>
        <div class="comp-desc">Functions that measure how wrong the model's predictions are by comparing them to the ground truth labels. They return a single scalar value — zero means perfect predictions; higher means worse. The training objective is to minimize this value. <strong style="color:#fff">Mean Squared Error (MSE)</strong> is standard for regression tasks; <strong style="color:#fff">Cross-Entropy Loss</strong> is used for classification.</div>
        <div class="comp-example">MSE: (1/n) Σ(predicted − actual)²<br>Cross-Entropy: −Σ y·log(ŷ)</div>
      </div>

      <div class="a2-comp-card highlight2">
        <span class="comp-icon">⚙️</span>
        <div class="comp-name">Component 06</div>
        <div class="comp-title">Optimization Algorithms</div>
        <div class="comp-desc">Algorithms that update the network's weights to minimize the loss function. They use the gradients calculated during backpropagation to decide how much to adjust each weight. <strong style="color:#fff">Gradient Descent</strong> is the foundation; <strong style="color:#fff">SGD</strong> updates from one sample at a time; <strong style="color:#fff">Adam</strong> adapts learning rates per-parameter and is the most widely used modern optimizer.</div>
        <div class="comp-example">new_weight = weight − (learning_rate × gradient)<br>Adam: adaptive per-parameter learning rates</div>
      </div>

    </div>

    <!-- ── ARCHITECTURE DIAGRAM ─────────────────────── -->
    <div class="a2-diagram-wrap">
      <div class="a2-diagram-title">▸ Neural Network Architecture — Data Flow Diagram</div>
      <svg class="nn-diagram" viewBox="0 0 960 360" xmlns="http://www.w3.org/2000/svg" aria-label="Neural network architecture diagram showing input, hidden, and output layers">

        <!-- Connection lines (drawn first, behind neurons) -->
        <!-- Input → Hidden1 -->
        <g stroke="#1E3A5A" stroke-width="1.2" opacity="0.8">
          <!-- i0 → h0,h1,h2,h3 -->
          <line x1="168" y1="100" x2="368" y2="72"/><line x1="168" y1="100" x2="368" y2="132"/>
          <line x1="168" y1="100" x2="368" y2="192"/><line x1="168" y1="100" x2="368" y2="252"/>
          <!-- i1 → h0,h1,h2,h3 -->
          <line x1="168" y1="180" x2="368" y2="72"/><line x1="168" y1="180" x2="368" y2="132"/>
          <line x1="168" y1="180" x2="368" y2="192"/><line x1="168" y1="180" x2="368" y2="252"/>
          <!-- i2 → h0,h1,h2,h3 -->
          <line x1="168" y1="260" x2="368" y2="72"/><line x1="168" y1="260" x2="368" y2="132"/>
          <line x1="168" y1="260" x2="368" y2="192"/><line x1="168" y1="260" x2="368" y2="252"/>
        </g>
        <!-- Hidden1 → Hidden2 -->
        <g stroke="#1E3A5A" stroke-width="1.2" opacity="0.8">
          <line x1="432" y1="72"  x2="592" y2="72"/> <line x1="432" y1="72"  x2="592" y2="152"/>
          <line x1="432" y1="72"  x2="592" y2="232"/><line x1="432" y1="132" x2="592" y2="72"/>
          <line x1="432" y1="132" x2="592" y2="152"/><line x1="432" y1="132" x2="592" y2="232"/>
          <line x1="432" y1="192" x2="592" y2="72"/> <line x1="432" y1="192" x2="592" y2="152"/>
          <line x1="432" y1="192" x2="592" y2="232"/><line x1="432" y1="252" x2="592" y2="72"/>
          <line x1="432" y1="252" x2="592" y2="152"/><line x1="432" y1="252" x2="592" y2="232"/>
        </g>
        <!-- Hidden2 → Output -->
        <g stroke="#1E3A5A" stroke-width="1.2" opacity="0.8">
          <line x1="656" y1="72"  x2="816" y2="140"/><line x1="656" y1="72"  x2="816" y2="220"/>
          <line x1="656" y1="152" x2="816" y2="140"/><line x1="656" y1="152" x2="816" y2="220"/>
          <line x1="656" y1="232" x2="816" y2="140"/><line x1="656" y1="232" x2="816" y2="220"/>
        </g>

        <!-- Layer label boxes -->
        <!-- Input -->
        <rect x="104" y="24" width="128" height="36" rx="3" fill="#132035" stroke="#34D399" stroke-width="1.5"/>
        <text x="168" y="47" text-anchor="middle" font-family="'Space Mono', monospace" font-size="10" fill="#34D399" letter-spacing="1">INPUT LAYER</text>
        <!-- Hidden 1 -->
        <rect x="304" y="24" width="128" height="36" rx="3" fill="#132035" stroke="#06B6D4" stroke-width="1.5"/>
        <text x="368" y="47" text-anchor="middle" font-family="'Space Mono', monospace" font-size="10" fill="#06B6D4" letter-spacing="1">HIDDEN L1</text>
        <!-- Hidden 2 -->
        <rect x="528" y="24" width="128" height="36" rx="3" fill="#132035" stroke="#06B6D4" stroke-width="1.5"/>
        <text x="592" y="47" text-anchor="middle" font-family="'Space Mono', monospace" font-size="10" fill="#06B6D4" letter-spacing="1">HIDDEN L2</text>
        <!-- Output -->
        <rect x="752" y="24" width="128" height="36" rx="3" fill="#132035" stroke="#34D399" stroke-width="1.5"/>
        <text x="816" y="47" text-anchor="middle" font-family="'Space Mono', monospace" font-size="10" fill="#34D399" letter-spacing="1">OUTPUT LAYER</text>

        <!-- Input neurons (3) -->
        <g fill="#0D2240" stroke="#34D399" stroke-width="2">
          <circle cx="168" cy="100" r="26"/><circle cx="168" cy="180" r="26"/><circle cx="168" cy="260" r="26"/>
        </g>
        <!-- Input labels -->
        <g font-family="'Space Mono', monospace" font-size="10" fill="#34D399" text-anchor="middle">
          <text x="168" y="104">x₁</text><text x="168" y="184">x₂</text><text x="168" y="264">x₃</text>
        </g>

        <!-- Hidden1 neurons (4) -->
        <g fill="#0D2240" stroke="#06B6D4" stroke-width="2">
          <circle cx="368" cy="72" r="26"/><circle cx="368" cy="132" r="26"/>
          <circle cx="368" cy="192" r="26"/><circle cx="368" cy="252" r="26"/>
        </g>
        <!-- Hidden1 labels -->
        <g font-family="'Space Mono', monospace" font-size="9" fill="#06B6D4" text-anchor="middle">
          <text x="368" y="76">h₁</text><text x="368" y="136">h₂</text>
          <text x="368" y="196">h₃</text><text x="368" y="256">h₄</text>
        </g>

        <!-- Hidden2 neurons (3) -->
        <g fill="#0D2240" stroke="#06B6D4" stroke-width="2">
          <circle cx="592" cy="72" r="26"/><circle cx="592" cy="152" r="26"/><circle cx="592" cy="232" r="26"/>
        </g>
        <g font-family="'Space Mono', monospace" font-size="9" fill="#06B6D4" text-anchor="middle">
          <text x="592" y="76">h₁</text><text x="592" y="156">h₂</text><text x="592" y="236">h₃</text>
        </g>

        <!-- Output neurons (2) -->
        <g fill="#0D2240" stroke="#34D399" stroke-width="2">
          <circle cx="816" cy="140" r="26"/><circle cx="816" cy="220" r="26"/>
        </g>
        <g font-family="'Space Mono', monospace" font-size="9" fill="#34D399" text-anchor="middle">
          <text x="816" y="144">ŷ₁</text><text x="816" y="224">ŷ₂</text>
        </g>

        <!-- Side annotations -->
        <text x="40" y="170" text-anchor="middle" font-family="'DM Sans', sans-serif" font-size="10" fill="#64748B">Raw<br/>features</text>
        <text x="900" y="170" text-anchor="middle" font-family="'DM Sans', sans-serif" font-size="10" fill="#64748B">Class<br/>scores</text>

        <!-- Data flow caption -->
        <line x1="60" y1="320" x2="900" y2="320" stroke="#0E7490" stroke-width="1" stroke-dasharray="6,4"/>
        <text x="480" y="340" text-anchor="middle" font-family="'DM Sans', sans-serif" font-size="11" fill="#64748B">← Data flows forward through layers; gradients flow backward during training →</text>

        <!-- Weight annotation -->
        <text x="270" y="108" text-anchor="middle" font-family="'Space Mono', monospace" font-size="8.5" fill="#C9A84C">w</text>
        <text x="270" y="118" text-anchor="middle" font-family="'Space Mono', monospace" font-size="7" fill="#94A3B8">weights</text>
      </svg>
    </div>

    <!-- ── TRAINING LOOP ─────────────────────────────── -->
    <div class="a2-loop-title">▸ The Training Loop — How Neural Networks Learn</div>
    <div class="a2-training-loop">
      <div class="loop-step">
        <div class="loop-step-inner">
          <div class="loop-num">1</div>
          <div class="loop-step-name">Input Data</div>
          <div class="loop-step-desc">Feed batch of features into the input layer neurons</div>
        </div>
        <div class="loop-arrow">›</div>
      </div>
      <div class="loop-step">
        <div class="loop-step-inner">
          <div class="loop-num">2</div>
          <div class="loop-step-name">Forward Pass</div>
          <div class="loop-step-desc">Data flows through layers; activations fire at each neuron</div>
        </div>
        <div class="loop-arrow">›</div>
      </div>
      <div class="loop-step">
        <div class="loop-step-inner">
          <div class="loop-num">3</div>
          <div class="loop-step-name">Compute Loss</div>
          <div class="loop-step-desc">Compare network output to ground truth; measure error</div>
        </div>
        <div class="loop-arrow">›</div>
      </div>
      <div class="loop-step">
        <div class="loop-step-inner">
          <div class="loop-num">4</div>
          <div class="loop-step-name">Backpropagation</div>
          <div class="loop-step-desc">Calculate gradients — how much each weight contributed to the error</div>
        </div>
        <div class="loop-arrow">›</div>
      </div>
      <div class="loop-step">
        <div class="loop-step-inner">
          <div class="loop-num">5</div>
          <div class="loop-step-name">Update Weights</div>
          <div class="loop-step-desc">Optimizer adjusts all weights to reduce loss slightly</div>
        </div>
      </div>
    </div>
    <div class="loop-repeat">↻ &nbsp; REPEAT FOR EACH BATCH &nbsp;·&nbsp; UNTIL LOSS CONVERGES &nbsp;·&nbsp; UNTIL TRAINING IS COMPLETE</div>

    <!-- ── SUMMARY / INSIGHTS ────────────────────────── -->
    <div class="a2-summary-title">▸ Summary — Why Visualizing Neural Networks Matters</div>
    <div class="a2-insights">
      <div class="a2-insight">
        <h4>Abstraction Through Structure</h4>
        <p>Each layer progressively extracts higher-level patterns — pixels → edges → shapes → objects. Visualizing this hierarchy makes the "black box" of deep learning understandable and communicable to any audience.</p>
      </div>
      <div class="a2-insight">
        <h4>Numbers Drive Learning</h4>
        <p>Weights and biases are the learnable memory of the network. Every fact the model knows about the world is encoded as a number on a connection. Visualizing weights reveals what the model has actually learned.</p>
      </div>
      <div class="a2-insight">
        <h4>Non-Linearity is Essential</h4>
        <p>Without activation functions, stacking layers is mathematically redundant. They are what allows neural networks to model the complex, non-linear patterns present in real-world data like images and language.</p>
      </div>
      <div class="a2-insight">
        <h4>Loss &amp; Optimization: Two Sides of Learning</h4>
        <p>The loss function is the compass; optimization is the engine. Together they steer the network toward accuracy over thousands of iterations. Understanding both is essential to debugging and improving any model.</p>
      </div>
    </div>

    <!-- Download note -->
    <div class="a2-download">
      <p>This artifact is also available as a <strong>professional PowerPoint presentation</strong> (.pptx) with custom diagrams, dark-ocean design theme, and full component breakdowns — suitable for direct submission or portfolio embedding.</p>
      <div class="a2-dl-label">Presentation Available</div>
    </div>

  </div>
</section>

<div class="artifact-divider"></div>

<!-- PROCESS -->
<section class="process-section" id="process">
  <div class="section-label">How These Artifacts Were Created</div>
  <div class="section-title">My <span>Process</span></div>
  <div class="divider"></div>
  <div class="process-steps">
    <div class="process-step">
      <div class="step-num">01</div>
      <div class="step-title">Research</div>
      <p>Reviewed course materials, IWU resources, and supplementary content on ML algorithms and neural network components across supervised, unsupervised, and generative domains.</p>
    </div>
    <div class="process-step">
      <div class="step-num">02</div>
      <div class="step-title">Experiment</div>
      <p>Used the TensorFlow Neural Network Playground to directly observe how layers, neurons, activation functions, noise, and learning rates interact during training.</p>
    </div>
    <div class="process-step">
      <div class="step-num">03</div>
      <div class="step-title">Design</div>
      <p>Built comparative frameworks, network architecture diagrams, component cards, and training loop visuals to present information accessibly for both technical and non-technical audiences.</p>
    </div>
    <div class="process-step">
      <div class="step-num">04</div>
      <div class="step-title">Synthesize</div>
      <p>Connected each component to real-world examples and practical implications. Added summary insights to anchor abstract concepts in outcomes that matter to organizations and practitioners.</p>
    </div>
  </div>
</section>

<!-- TOOLS -->
<section class="tools-section">
  <div class="section-label">Tools &amp; Technologies</div>
  <div class="section-title">What I <span>Used</span></div>
  <div class="divider"></div>
  <div class="tools-grid">
    <div class="tool-chip">HTML / CSS</div>
    <div class="tool-chip">TensorFlow Playground</div>
    <div class="tool-chip">Research Synthesis</div>
    <div class="tool-chip">Visual Framework Design</div>
    <div class="tool-chip">SVG Diagram Design</div>
    <div class="tool-chip">Generative AI Tools</div>
    <div class="tool-chip">Comparative Matrix</div>
    <div class="tool-chip">Use Case Analysis</div>
    <div class="tool-chip">PowerPoint (pptxgenjs)</div>
    <div class="tool-chip">Academic Coursework (IWU)</div>
    <div class="tool-chip">Portfolio Documentation</div>
  </div>
</section>

<!-- FOOTER -->
<footer>
  <p><span>Mohsin Syed Ali</span> · AIML Professional Portfolio · Indiana Wesleyan University · 2025</p>
  <div class="footer-artifacts">
    <div class="footer-artifact">
      <strong>Artifact 01</strong>
      Machine Learning Algorithm Visual Framework · Course Assignment
    </div>
    <div class="footer-artifact art2">
      <strong>Artifact 02</strong>
      Neural Networks: Structure &amp; Components · Course Assignment
    </div>
  </div>
</footer>

</body>
</html>
