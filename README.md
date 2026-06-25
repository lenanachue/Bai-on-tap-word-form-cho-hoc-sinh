<!DOCTYPE html>
<html lang="vi">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Word Forms – Bài Học & Ôn Tập Gợi Nhớ</title>
<style>
@import url('https://fonts.googleapis.com/css2?family=Nunito:wght@400;600;700;800;900&family=Playfair+Display:wght@700;900&display=swap');

:root {
  --lavender:      #c4aee8;
  --lavender-mid:  #9b7fcc;
  --lavender-deep: #6a4c9c;
  --plum:          #4a2c7a;
  --lilac:         #e8dff7;
  --lilac-pale:    #f5f1fc;
  --lilac-soft:    #ede5f8;
  --rose:          #f0c4e0;
  --rose-pale:     #fdf0f8;
  --mint-purple:   #d4c8f0;
  --gold-soft:     #f7e8b0;
  --gold:          #d4a017;
  --ink:           #2a1a4a;
  --ink-mid:       #4a3570;
  --ink-light:     #7a6095;
  --border:        #d8caf0;
  --white:         #ffffff;
  --correct-bg:    #e0f7ea;
  --correct-text:  #1b6e3e;
  --wrong-bg:      #fde8e8;
  --wrong-text:    #b91c1c;
}

*, *::before, *::after { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }

body {
  font-family: 'Nunito', sans-serif;
  background: var(--lilac-pale);
  color: var(--ink);
  min-height: 100vh;
  overflow-x: hidden;
}

/* ── HERO ── */
.hero {
  position: relative;
  background: linear-gradient(145deg, var(--plum) 0%, var(--lavender-deep) 45%, var(--lavender-mid) 100%);
  padding: 52px 24px 110px;
  text-align: center;
  overflow: hidden;
}
.hero::after {
  content: '';
  position: absolute;
  bottom: -2px; left: 0; right: 0; height: 68px;
  background: url("data:image/svg+xml,%3Csvg xmlns='http://www.w3.org/2000/svg' viewBox='0 0 1440 68'%3E%3Cpath fill='%23f5f1fc' d='M0,40 C200,10 400,60 600,30 C800,0 1000,55 1200,28 C1340,10 1400,40 1440,30 L1440,68 L0,68Z'/%3E%3C/svg%3E") center/cover no-repeat;
}

/* Floating stationery decorations */
.deco-item {
  position: absolute;
  pointer-events: none;
  opacity: 0.18;
  animation: float-deco 6s ease-in-out infinite;
  font-size: 2rem;
}
.deco-item:nth-child(1)  { top: 12%; left: 5%;  animation-delay: 0s;   font-size: 2.4rem; }
.deco-item:nth-child(2)  { top: 25%; left: 14%; animation-delay: 1.2s; }
.deco-item:nth-child(3)  { top: 8%;  left: 78%; animation-delay: 0.5s; font-size: 2.8rem; }
.deco-item:nth-child(4)  { top: 60%; left: 88%; animation-delay: 2s;   font-size: 1.8rem; }
.deco-item:nth-child(5)  { top: 70%; left: 6%;  animation-delay: 1.5s; font-size: 1.6rem; }
.deco-item:nth-child(6)  { top: 50%; left: 92%; animation-delay: 0.8s; }
.deco-item:nth-child(7)  { top: 20%; left: 90%; animation-delay: 3s;   font-size: 1.5rem; }
.deco-item:nth-child(8)  { top: 80%; left: 40%; animation-delay: 2.5s; font-size: 1.4rem; }
@keyframes float-deco {
  0%, 100% { transform: translateY(0px) rotate(0deg); }
  50%       { transform: translateY(-12px) rotate(6deg); }
}

/* Sparkle dots */
.sparkles { position: absolute; inset: 0; pointer-events: none; }
.sparkle {
  position: absolute; border-radius: 50%;
  background: rgba(255,255,255,.55);
  animation: twinkle 3s infinite ease-in-out;
}
.sparkle:nth-child(1) { width:5px; height:5px; top:18%; left:22%; animation-delay:0s; }
.sparkle:nth-child(2) { width:3px; height:3px; top:45%; left:35%; animation-delay:0.7s; }
.sparkle:nth-child(3) { width:6px; height:6px; top:30%; left:60%; animation-delay:1.2s; }
.sparkle:nth-child(4) { width:4px; height:4px; top:65%; left:70%; animation-delay:0.4s; }
.sparkle:nth-child(5) { width:5px; height:5px; top:15%; left:50%; animation-delay:1.8s; }
@keyframes twinkle {
  0%, 100% { opacity: 0.3; transform: scale(1); }
  50%       { opacity: 1;   transform: scale(1.6); }
}

.hero-badge {
  display: inline-block;
  background: rgba(255,255,255,.15);
  border: 1px solid rgba(255,255,255,.3);
  color: var(--lilac); font-size: .75rem; font-weight:800;
  letter-spacing:.12em; text-transform: uppercase;
  padding: 5px 16px; border-radius: 20px; margin-bottom: 20px;
}
.hero h1 {
  font-family: 'Playfair Display', serif;
  font-size: clamp(2rem, 5.5vw, 3.4rem);
  color: var(--white); line-height: 1.2; font-weight: 900;
  text-shadow: 0 3px 16px rgba(0,0,0,.3);
  margin-bottom: 12px;
}
.hero h1 span { color: var(--gold-soft); }
.hero p {
  color: var(--lilac); font-size: 1.05rem;
  max-width: 580px; margin: 0 auto 28px; line-height: 1.8;
}
.hero-deco { font-size: 2.6rem; letter-spacing: 10px; }

/* ── NAV ── */
.nav-wrap {
  background: var(--white);
  border-bottom: 2px solid var(--border);
  position: sticky; top: 0; z-index: 99;
}
.nav-pills {
  display: flex; gap: 6px; overflow-x: auto;
  padding: 10px 20px; max-width: 1100px;
  margin: 0 auto; scrollbar-width: none;
}
.nav-pills::-webkit-scrollbar { display: none; }
.nav-pill {
  flex-shrink: 0; padding: 6px 16px;
  border-radius: 20px; font-size: .84rem; font-weight: 800;
  cursor: pointer; border: 2px solid var(--border);
  background: var(--lilac-pale); color: var(--ink-light);
  transition: all .2s; text-decoration: none; display: inline-block;
}
.nav-pill:hover, .nav-pill.active {
  background: var(--lavender-deep); color: var(--white);
  border-color: var(--lavender-deep);
}

/* ── LAYOUT ── */
.main { max-width: 1000px; margin: 0 auto; padding: 40px 20px 80px; }

/* ── SCIENCE BANNER ── */
.science-banner {
  background: linear-gradient(135deg, var(--plum), var(--lavender-deep));
  color: var(--white);
  border-radius: 18px; padding: 22px 28px;
  margin-bottom: 36px;
  display: grid; grid-template-columns: auto 1fr;
  gap: 18px; align-items: center;
  box-shadow: 0 8px 30px rgba(74,44,122,.2);
}
.science-brain { font-size: 3rem; }
.science-text h3 {
  font-size: 1.1rem; font-weight: 900;
  margin-bottom: 6px; color: var(--gold-soft);
}
.science-text p { font-size: .88rem; line-height: 1.8; opacity: .9; }
.science-tags { display: flex; flex-wrap: wrap; gap: 6px; margin-top: 10px; }
.sci-tag {
  background: rgba(255,255,255,.15);
  border: 1px solid rgba(255,255,255,.3);
  color: var(--lilac); font-size: .72rem; font-weight: 800;
  padding: 3px 10px; border-radius: 12px;
  letter-spacing: .04em;
}

/* ── SECTION TITLES ── */
.section-title {
  display: flex; align-items: center; gap: 12px;
  font-size: 1.5rem; font-weight: 900; color: var(--plum);
  margin: 52px 0 22px; padding-bottom: 10px;
  border-bottom: 3px solid var(--lavender);
}
.section-title .icon { font-size: 1.8rem; }

.subsec-label {
  display: inline-flex; align-items: center; gap: 8px;
  font-size: .72rem; font-weight: 800; letter-spacing: .1em;
  text-transform: uppercase; color: var(--lavender-deep);
  background: var(--lilac-soft); border: 1.5px solid var(--border);
  padding: 4px 14px; border-radius: 12px;
  margin-bottom: 14px;
}

.subsection-title {
  font-size: 1.1rem; font-weight: 900; color: var(--lavender-deep);
  margin: 28px 0 14px; padding-left: 14px;
  border-left: 4px solid var(--lavender-mid);
}

/* ── PHASE CHIP ── */
.phase-chip {
  display: inline-flex; align-items: center; gap: 6px;
  font-size: .7rem; font-weight: 800; letter-spacing: .08em;
  text-transform: uppercase; padding: 3px 12px;
  border-radius: 12px; margin-bottom: 16px;
}
.chip-learn  { background: var(--lilac-soft); color: var(--lavender-deep); border: 1.5px solid var(--border); }
.chip-recall { background: #fef9e7; color: #856404; border: 1.5px solid #f0d96c; }
.chip-test   { background: #eafaf1; color: #1b6e3e; border: 1.5px solid #7fe0a3; }

/* ── THEORY CARD ── */
.theory-card {
  background: var(--white);
  border-radius: 18px;
  border: 1.5px solid var(--border);
  box-shadow: 0 4px 20px rgba(100,76,156,.07);
  padding: 28px 26px 24px;
  margin-bottom: 22px;
  transition: box-shadow .2s;
}
.theory-card:hover { box-shadow: 0 8px 32px rgba(100,76,156,.13); }

/* ── RULE GRID ── */
.rule-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(270px, 1fr));
  gap: 14px; margin-top: 10px;
}
.rule-item {
  background: var(--lilac-pale);
  border: 1.5px solid var(--border);
  border-radius: 14px; padding: 14px 16px;
  transition: transform .15s, box-shadow .15s;
}
.rule-item:hover {
  transform: translateY(-2px);
  box-shadow: 0 6px 18px rgba(100,76,156,.12);
}
.rule-formula {
  font-size: .87rem; font-weight: 900; color: var(--lavender-deep);
  font-family: monospace;
  background: var(--lilac-soft); padding: 4px 10px;
  border-radius: 7px; display: inline-block; margin-bottom: 8px;
}
.suffix-hi { color: var(--lavender-mid); }
.verb-hi   { color: #2e7d32; }
.adj-hi    { color: #b45309; }
.adv-hi    { color: #9d174d; }

.rule-example { font-size: .85rem; color: var(--ink-light); line-height: 1.7; }
.ex-arrow { color: var(--lavender); font-weight: 900; margin: 0 4px; }

/* ── WORD FAMILY TABLE ── */
.wf-table {
  width: 100%; border-collapse: collapse;
  font-size: .9rem; margin-top: 10px;
}
.wf-table th {
  background: linear-gradient(90deg, var(--lavender-deep), var(--lavender-mid));
  color: var(--white); padding: 10px 14px; text-align: left;
  font-weight: 800;
}
.wf-table th:first-child { border-radius: 8px 0 0 0; }
.wf-table th:last-child  { border-radius: 0 8px 0 0; }
.wf-table td {
  padding: 9px 14px; border-bottom: 1px solid var(--border);
  vertical-align: middle; line-height: 1.6;
}
.wf-table tr:nth-child(even) td { background: var(--lilac-pale); }
.pos-chip {
  display: inline-block; font-size: .72rem; font-weight: 800;
  padding: 2px 9px; border-radius: 10px; margin-right: 4px;
}
.pos-n   { background: #dbeafe; color: #1d4ed8; }
.pos-v   { background: #dcfce7; color: #166534; }
.pos-a   { background: #fef3c7; color: #92400e; }
.pos-adv { background: #fce7f3; color: #9d174d; }
.wf-root { font-weight: 900; color: var(--plum); }

/* ── CONTEXT SIGNAL TABLE ── */
.ctx-table { width: 100%; border-collapse: collapse; font-size: .9rem; }
.ctx-table th {
  background: var(--lavender-mid); color: var(--white);
  padding: 10px 14px; text-align: left; font-weight: 800;
}
.ctx-table th:first-child { border-radius: 8px 0 0 0; }
.ctx-table th:last-child  { border-radius: 0 8px 0 0; }
.ctx-table td { padding: 9px 14px; border-bottom: 1px solid var(--border); line-height: 1.6; }
.ctx-table tr:nth-child(even) td { background: var(--lilac-pale); }
.ctx-signal { font-family: monospace; font-weight: 800; color: var(--lavender-deep); }
.ctx-pos    { font-weight: 800; color: var(--plum); }

/* ── NOTE BOX ── */
.note-box {
  background: linear-gradient(135deg, var(--lilac-soft), var(--lilac-pale));
  border-left: 4px solid var(--lavender-mid);
  border-radius: 0 14px 14px 0;
  padding: 16px 18px; margin: 18px 0;
  font-size: .9rem; color: var(--ink-mid); line-height: 1.9;
}
.note-box strong { color: var(--plum); }

/* ── MNEMONIC CARD ── */
.mnemonic-grid {
  display: grid;
  grid-template-columns: repeat(auto-fill, minmax(220px, 1fr));
  gap: 14px; margin-top: 10px;
}
.mnemonic-card {
  border-radius: 16px; padding: 18px 16px;
  text-align: center;
  border: 2px solid transparent;
  transition: transform .15s;
}
.mnemonic-card:hover { transform: translateY(-3px); }
.mnemonic-card.noun { background: linear-gradient(135deg,#dbeafe,#c7d9f7); border-color: #93c5fd; }
.mnemonic-card.verb { background: linear-gradient(135deg,#dcfce7,#c3f0d0); border-color: #86efac; }
.mnemonic-card.adj  { background: linear-gradient(135deg,#fef3c7,#fde99a); border-color: #fcd34d; }
.mnemonic-card.adv  { background: linear-gradient(135deg,#fce7f3,#f8cfe8); border-color: #f9a8d4; }
.mn-icon { font-size: 2rem; margin-bottom: 8px; }
.mn-label {
  font-size: .72rem; font-weight: 900; letter-spacing: .1em;
  text-transform: uppercase; margin-bottom: 10px;
  opacity: .75;
}
.mnemonic-card.noun .mn-label { color: #1d4ed8; }
.mnemonic-card.verb .mn-label { color: #166534; }
.mnemonic-card.adj  .mn-label { color: #92400e; }
.mnemonic-card.adv  .mn-label { color: #9d174d; }
.mn-suffix {
  display: inline-block; font-size: .8rem; font-weight: 900;
  font-family: monospace; padding: 3px 10px;
  border-radius: 12px; margin: 3px;
}
.mnemonic-card.noun .mn-suffix { background: #1d4ed8; color: #fff; }
.mnemonic-card.verb .mn-suffix { background: #166534; color: #fff; }
.mnemonic-card.adj  .mn-suffix { background: #92400e; color: #fff; }
.mnemonic-card.adv  .mn-suffix { background: #9d174d; color: #fff; }
.mn-tip {
  margin-top: 10px; font-size: .78rem; line-height: 1.6;
  opacity: .8; font-style: italic;
}

/* ── MIND-MAP SVG DIAGRAM ── */
.diagram-wrap {
  background: var(--white); border-radius: 20px;
  border: 2px solid var(--border);
  padding: 28px 20px 20px;
  box-shadow: 0 4px 24px rgba(100,76,156,.08);
  overflow-x: auto; margin-bottom: 24px;
}
.diagram-wrap svg { max-width: 100%; height: auto; display: block; margin: 0 auto; }

/* ── QUIZ BOX ── */
.quiz-box {
  background: linear-gradient(135deg, #fdf6ff, #f8f0ff);
  border: 2px solid var(--lavender);
  border-radius: 18px; padding: 24px 26px; margin: 28px 0;
}
.quiz-title {
  font-size: 1rem; font-weight: 900; color: var(--plum);
  margin-bottom: 6px; display: flex; align-items: center; gap: 8px;
}
.quiz-sci { font-size: .72rem; font-weight: 800; color: var(--ink-light); opacity: .7; margin-bottom: 18px; }
.quiz-question { margin-bottom: 18px; }
.quiz-question p {
  font-size: .95rem; font-weight: 700; color: var(--ink);
  margin-bottom: 10px; line-height: 1.6;
}
.quiz-options { display: flex; flex-wrap: wrap; gap: 8px; }
.quiz-opt {
  padding: 7px 18px; border-radius: 20px;
  border: 2px solid var(--border);
  background: var(--white); font-size: .88rem; font-weight: 700;
  cursor: pointer; color: var(--ink-mid);
  transition: all .18s;
}
.quiz-opt:hover    { border-color: var(--lavender-mid); color: var(--lavender-deep); }
.quiz-opt.correct  { background: var(--correct-bg); border-color: #34c768; color: var(--correct-text); }
.quiz-opt.wrong    { background: var(--wrong-bg); border-color: #dc2626; color: var(--wrong-text); }
.quiz-opt:disabled { cursor: default; }
.quiz-feedback {
  font-size: .88rem; font-weight: 700; margin-top: 8px;
  padding: 6px 12px; border-radius: 8px; display: none;
  line-height: 1.6;
}
.quiz-feedback.show { display: block; }
.quiz-feedback.ok  { background: var(--correct-bg); color: var(--correct-text); }
.quiz-feedback.err { background: var(--wrong-bg);   color: var(--wrong-text); }

/* ── SPACED RECALL SECTION ── */
.recall-box {
  background: linear-gradient(135deg, #fffbeb, #fef9e7);
  border: 2px solid #f0d96c;
  border-radius: 18px; padding: 24px 26px; margin: 28px 0;
}
.recall-title {
  font-size: 1rem; font-weight: 900; color: #7c5800;
  margin-bottom: 6px; display: flex; align-items: center; gap: 8px;
}
.recall-sci { font-size: .72rem; color: #7c5800; opacity: .7; margin-bottom: 18px; }
.recall-item {
  background: var(--white); border: 1.5px solid #f0d96c;
  border-radius: 12px; padding: 16px 18px; margin-bottom: 14px;
}
.recall-q { font-size: .95rem; font-weight: 700; color: var(--ink); margin-bottom: 10px; }
.recall-input-row { display: flex; gap: 10px; flex-wrap: wrap; align-items: center; }
.recall-input {
  border: 2px solid var(--border); border-radius: 10px;
  padding: 8px 14px; font-size: .95rem; font-family: 'Nunito', sans-serif;
  font-weight: 700; color: var(--ink);
  width: 160px; outline: none; transition: border-color .2s;
}
.recall-input:focus { border-color: var(--lavender-mid); }
.recall-input.ok    { border-color: #34c768; background: var(--correct-bg); color: var(--correct-text); }
.recall-input.err   { border-color: #dc2626; background: var(--wrong-bg); color: var(--wrong-text); }
.recall-check {
  padding: 8px 20px; border-radius: 16px;
  background: var(--lavender-deep); color: var(--white);
  border: none; font-size: .88rem; font-weight: 800;
  cursor: pointer; transition: all .2s;
}
.recall-check:hover { background: var(--plum); transform: translateY(-1px); }
.recall-hint {
  font-size: .8rem; color: var(--ink-light);
  margin-top: 8px; display: none;
}
.recall-hint.show { display: block; }
.reveal-btn {
  padding: 4px 14px; border-radius: 12px;
  background: var(--lilac-soft); color: var(--lavender-deep);
  border: 1.5px solid var(--border); font-size: .78rem;
  font-weight: 800; cursor: pointer;
}

/* ── EXERCISE SECTION ── */
.exercise-wrap {
  border-radius: 18px; overflow: hidden;
  margin-bottom: 28px;
  box-shadow: 0 4px 20px rgba(100,76,156,.1);
}
.exercise-head {
  background: linear-gradient(135deg, var(--plum), var(--lavender-deep));
  color: var(--white); padding: 18px 24px;
  display: flex; align-items: center; gap: 12px;
}
.exercise-head h3 { font-size: 1.1rem; font-weight: 900; }
.exercise-head .sci-badge {
  margin-left: auto; background: rgba(255,255,255,.18);
  font-size: .7rem; font-weight: 800; padding: 3px 10px;
  border-radius: 10px; border: 1px solid rgba(255,255,255,.3);
}
.exercise-body {
  background: var(--white);
  border: 1.5px solid var(--border); border-top: none;
  border-radius: 0 0 18px 18px; padding: 24px;
}

.ex-q {
  display: flex; gap: 12px; margin-bottom: 20px;
  align-items: flex-start;
}
.ex-num {
  min-width: 32px; height: 32px; border-radius: 50%;
  background: linear-gradient(135deg, var(--lavender-mid), var(--lavender-deep));
  color: var(--white); display: flex; align-items: center;
  justify-content: center; font-size: .85rem; font-weight: 900;
  flex-shrink: 0; margin-top: 2px;
}
.ex-content { flex: 1; }
.ex-sentence {
  font-size: .95rem; color: var(--ink); font-weight: 600;
  margin-bottom: 10px; line-height: 1.6;
}
.ex-opts { display: flex; flex-wrap: wrap; gap: 8px; }
.ex-opt {
  padding: 6px 16px; border-radius: 18px;
  border: 2px solid var(--border); background: var(--white);
  font-size: .88rem; font-weight: 700; cursor: pointer;
  color: var(--ink-mid); transition: all .18s;
}
.ex-opt:hover    { border-color: var(--lavender-mid); color: var(--lavender-deep); }
.ex-opt.correct  { background: var(--correct-bg); border-color: #34c768; color: var(--correct-text); pointer-events: none; }
.ex-opt.wrong    { background: var(--wrong-bg); border-color: #dc2626; color: var(--wrong-text); }
.ex-opt:disabled { cursor: default; }
.ex-fb {
  font-size: .83rem; margin-top: 6px; display: none;
  padding: 5px 10px; border-radius: 8px;
  font-weight: 700; line-height: 1.5;
}
.ex-fb.show { display: block; }
.ex-fb.ok   { background: var(--correct-bg); color: var(--correct-text); }
.ex-fb.err  { background: var(--wrong-bg);   color: var(--wrong-text); }

/* Score bar */
.score-bar {
  background: var(--lilac-soft); border: 1.5px solid var(--border);
  border-radius: 14px; padding: 16px 22px;
  margin-top: 12px; display: none;
  align-items: center; gap: 18px;
}
.score-num   { font-size: 1.6rem; font-weight: 900; color: var(--plum); }
.score-label { font-size: .85rem; color: var(--ink-light); font-weight: 700; }
.score-msg   { font-size: .88rem; color: var(--ink-mid); }

/* Total score */
.total-score-box {
  background: linear-gradient(135deg, var(--plum), var(--lavender-mid));
  border-radius: 22px; padding: 30px 28px;
  text-align: center; color: var(--white);
  margin-top: 20px; display: none;
  box-shadow: 0 8px 30px rgba(74,44,122,.25);
}

/* ── FOOTER ── */
.footer {
  background: var(--plum); color: var(--lilac);
  text-align: center; padding: 36px 20px;
  font-size: .88rem;
}
.footer-deco { font-size: 2rem; margin-bottom: 10px; letter-spacing: 8px; }

/* ── RESPONSIVE ── */
@media (max-width: 600px) {
  .rule-grid, .mnemonic-grid { grid-template-columns: 1fr; }
  .science-banner { grid-template-columns: 1fr; text-align: center; }
  .theory-card { padding: 18px 14px; }
  .exercise-body { padding: 16px; }
  .quiz-box, .recall-box { padding: 18px 16px; }
}
</style>
</head>
<body>

<!-- ═══ HERO ═══ -->
<header class="hero">
  <div class="deco-item">📚</div>
  <div class="deco-item">✏️</div>
  <div class="deco-item">📖</div>
  <div class="deco-item">🎒</div>
  <div class="deco-item">🖊️</div>
  <div class="deco-item">📐</div>
  <div class="deco-item">🔖</div>
  <div class="deco-item">📝</div>
  <div class="sparkles">
    <div class="sparkle"></div><div class="sparkle"></div>
    <div class="sparkle"></div><div class="sparkle"></div>
    <div class="sparkle"></div>
  </div>
  <div style="position:relative;z-index:2">
    <div class="hero-badge">📘 Tiếng Anh · Chuyên Đề Từ Vựng</div>
    <h1>Cấu Tạo Từ<br><span>Word Forms</span></h1>
    <p>Khám phá cách não bộ ghi nhớ từ vựng – học theo hệ thống, không học thuộc lòng. Mỗi từ gốc có thể sinh ra hàng chục từ mới!</p>
    <div class="hero-deco">📚 ✏️ 📖 🔖 📝</div>
  </div>
</header>

<!-- ═══ NAV ═══ -->
<nav class="nav-wrap">
  <div class="nav-pills">
    <a class="nav-pill" href="#hoc">📘 Học Lý Thuyết</a>
    <a class="nav-pill" href="#danh-tu">Danh Từ</a>
    <a class="nav-pill" href="#dong-tu">Động Từ</a>
    <a class="nav-pill" href="#tinh-tu">Tính Từ</a>
    <a class="nav-pill" href="#trang-tu">Trạng Từ</a>
    <a class="nav-pill" href="#nhan-biet">Nhận Biết</a>
    <a class="nav-pill" href="#so-do">🗺 Sơ Đồ</a>
    <a class="nav-pill" href="#goi-nho">🧠 Gợi Nhớ</a>
    <a class="nav-pill" href="#bai-tap">✏️ Bài Tập</a>
  </div>
</nav>

<!-- ═══ MAIN ═══ -->
<main class="main">

  <!-- Science intro banner -->
  <div class="science-banner">
    <div class="science-brain">🧠</div>
    <div class="science-text">
      <h3>Bài học này được thiết kế dựa trên khoa học não bộ</h3>
      <p>Thay vì chỉ đọc và nhớ, em sẽ trải qua 3 giai đoạn: <strong>Học lý thuyết có cấu trúc</strong> → <strong>Ôn tập gợi nhớ chủ động</strong> → <strong>Kiểm tra ứng dụng</strong>. Não bộ ghi nhớ tốt hơn khi phải tự tái tạo thông tin.</p>
      <div class="science-tags">
        <span class="sci-tag">📌 Semantic Clustering (Bower, 1969)</span>
        <span class="sci-tag">🔁 Retrieval Practice (Roediger &amp; Butler, 2011)</span>
        <span class="sci-tag">⚡ Generation Effect (Slamecka &amp; Graf, 1978)</span>
        <span class="sci-tag">🔍 Elaborative Interrogation (Pressley, 1992)</span>
      </div>
    </div>
  </div>

  <!-- ══════════════════════════════════
       PHẦN HỌC LÝ THUYẾT
  ══════════════════════════════════ -->
  <section id="hoc">
    <div class="section-title"><span class="icon">📘</span> Giai Đoạn 1 – Học Lý Thuyết</div>

    <div class="note-box">
      <strong>💡 Tại sao học Word Forms quan trọng?</strong><br>
      Tiếng Anh dùng <strong>hậu tố (suffix)</strong> và <strong>tiền tố (prefix)</strong> để chuyển một từ gốc thành nhiều từ loại.<br>
      Ví dụ: <strong>beauty</strong> (n) → <strong>beautiful</strong> (adj) → <strong>beautify</strong> (v) → <strong>beautifully</strong> (adv).<br>
      Học theo <em>hệ thống hậu tố</em> giúp não em phân loại thông tin theo nhóm – ghi nhớ sâu hơn nhiều lần so với học từng từ rời rạc.
      <br><small style="opacity:.65">→ Nguyên lý: <em>Semantic Clustering</em> (Bower et al., 1969) — nhóm từ cùng họ giúp tăng tỉ lệ nhớ lại lên đến 65%.</small>
    </div>

    <!-- ════ I. DANH TỪ ════ -->
    <div id="danh-tu" class="subsection-title">I. Cách tạo Danh Từ (Noun) 🪸</div>
    <div class="phase-chip chip-learn">📘 Pha Học · Đọc hiểu có chọn lọc</div>

    <div class="theory-card">
      <p style="font-size:.9rem;color:var(--ink-mid);margin-bottom:16px;">
        Danh từ thường được tạo bằng cách thêm <strong>hậu tố vào sau động từ hoặc tính từ</strong>.
        Màu <span style="color:var(--lavender-mid);font-weight:900;">tím</span> = phần hậu tố thêm vào.
      </p>

      <div style="font-size:.85rem;font-weight:800;color:var(--ink-light);margin-bottom:10px;text-transform:uppercase;letter-spacing:.06em;">Từ Động Từ → Danh Từ</div>
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-ment</span> → N</div>
          <div class="rule-example">
            develop → <strong>develop<span class="suffix-hi">ment</span></strong><br>
            entertain → <strong>entertain<span class="suffix-hi">ment</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-ance / -ence</span> → N</div>
          <div class="rule-example">
            attend → <strong>attend<span class="suffix-hi">ance</span></strong><br>
            depend → <strong>depend<span class="suffix-hi">ence</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-ion / -ation</span> → N</div>
          <div class="rule-example">
            invent → <strong>invent<span class="suffix-hi">ion</span></strong><br>
            inform → <strong>inform<span class="suffix-hi">ation</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-er / -or / -ar</span> → N <span style="font-size:.72rem;opacity:.65">(người làm)</span></div>
          <div class="rule-example">
            work → <strong>work<span class="suffix-hi">er</span></strong><br>
            act → <strong>act<span class="suffix-hi">or</span></strong> &nbsp;|&nbsp; lie → <strong>li<span class="suffix-hi">ar</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-ant / -ee / -ist</span> → N</div>
          <div class="rule-example">
            assist → <strong>assist<span class="suffix-hi">ant</span></strong><br>
            employ → <strong>employ<span class="suffix-hi">ee</span></strong> &nbsp;|&nbsp; type → <strong>typ<span class="suffix-hi">ist</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="suffix-hi">-al / -age / -ing</span> → N</div>
          <div class="rule-example">
            survive → <strong>surviv<span class="suffix-hi">al</span></strong><br>
            marry → <strong>marri<span class="suffix-hi">age</span></strong> &nbsp;|&nbsp; teach → <strong>teach<span class="suffix-hi">ing</span></strong>
          </div>
        </div>
      </div>

      <div style="font-size:.85rem;font-weight:800;color:var(--ink-light);margin: 20px 0 10px;text-transform:uppercase;letter-spacing:.06em;">Từ Tính Từ → Danh Từ</div>
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">Adj + <span class="suffix-hi">-ness</span> → N</div>
          <div class="rule-example">
            rich → <strong>rich<span class="suffix-hi">ness</span></strong><br>
            polite → <strong>polite<span class="suffix-hi">ness</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">Adj + <span class="suffix-hi">-ity / -ty / -cy</span> → N</div>
          <div class="rule-example">
            able → <strong>abil<span class="suffix-hi">ity</span></strong><br>
            certain → <strong>certain<span class="suffix-hi">ty</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">Adj + <span class="suffix-hi">-th / -dom</span> → N</div>
          <div class="rule-example">
            warm → <strong>warm<span class="suffix-hi">th</span></strong><br>
            free → <strong>free<span class="suffix-hi">dom</span></strong>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="suffix-hi">-hood / -ship</span> → N</div>
          <div class="rule-example">
            child → <strong>child<span class="suffix-hi">hood</span></strong><br>
            friend → <strong>friend<span class="suffix-hi">ship</span></strong>
          </div>
        </div>
      </div>
    </div>

    <!-- mini quiz 1 -->
    <div class="quiz-box">
      <div class="quiz-title">⚡ Kiểm Tra Nhanh – Danh Từ</div>
      <div class="quiz-sci">🔬 Generation Effect — tự chọn đáp án giúp não ghi nhớ sâu hơn đọc thụ động 2–3 lần (Slamecka &amp; Graf, 1978)</div>

      <div class="quiz-question" id="q1">
        <p>1. "develop" (v) → ______ (n) &nbsp;– cần hậu tố nào?</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q1" data-correct="true" data-msg="-ment → development ✅">-ment</button>
          <button class="quiz-opt" data-qid="q1" data-correct="false" data-msg="Đây là hậu tố tính từ, không phải danh từ từ động từ.">-ful</button>
          <button class="quiz-opt" data-qid="q1" data-correct="false" data-msg="-ive tạo tính từ, không phải danh từ.">-ive</button>
          <button class="quiz-opt" data-qid="q1" data-correct="false" data-msg="-ous tạo tính từ từ danh từ.">-ous</button>
        </div>
        <div class="quiz-feedback" id="fb-q1"></div>
      </div>

      <div class="quiz-question" id="q2">
        <p>2. "rich" (adj) → ______ (n)</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q2" data-correct="false" data-msg="-ity thường dùng với adj dài hơn: ability, nationality.">richity</button>
          <button class="quiz-opt" data-qid="q2" data-correct="true" data-msg="-ness + adj ngắn → richness ✅">richness</button>
          <button class="quiz-opt" data-qid="q2" data-correct="false" data-msg="Không phải từ hợp lệ trong tiếng Anh.">richdom</button>
          <button class="quiz-opt" data-qid="q2" data-correct="false" data-msg="Đây là trạng từ (adverb).">richly</button>
        </div>
        <div class="quiz-feedback" id="fb-q2"></div>
      </div>

      <div class="quiz-question" id="q3">
        <p>3. Từ nào là danh từ chỉ <strong>người</strong> trong nhóm sau?</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q3" data-correct="false" data-msg="arrival = sự đến – chỉ sự kiện, không chỉ người.">arrival</button>
          <button class="quiz-opt" data-qid="q3" data-correct="false" data-msg="invention = phát minh – chỉ sự vật, không chỉ người.">invention</button>
          <button class="quiz-opt" data-qid="q3" data-correct="true" data-msg="employer = người thuê → đuôi -er/-or/-ist chỉ người ✅">employer</button>
          <button class="quiz-opt" data-qid="q3" data-correct="false" data-msg="freedom = tự do – chỉ trạng thái, không chỉ người.">freedom</button>
        </div>
        <div class="quiz-feedback" id="fb-q3"></div>
      </div>
    </div>

    <!-- ════ II. ĐỘNG TỪ ════ -->
    <div id="dong-tu" class="subsection-title">II. Cách tạo Động Từ (Verb) 🌿</div>
    <div class="phase-chip chip-learn">📘 Pha Học · Đọc hiểu có chọn lọc</div>

    <div class="theory-card">
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">Adj + <span class="verb-hi">-en</span> → V</div>
          <div class="rule-example">
            wide → <strong>wid<span class="verb-hi">en</span></strong> (mở rộng)<br>
            short → <strong>short<span class="verb-hi">en</span></strong> (thu ngắn)
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula"><span class="verb-hi">en-</span> + Adj → V</div>
          <div class="rule-example">
            <span class="verb-hi">en</span>rich (làm giàu)<br>
            <span class="verb-hi">en</span>large (phóng to)
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N/Adj + <span class="verb-hi">-ise / -ize</span> → V</div>
          <div class="rule-example">
            social → social<span class="verb-hi">ize</span><br>
            industrial → industrial<span class="verb-hi">ize</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="verb-hi">-ify / -fy</span> → V</div>
          <div class="rule-example">
            beauty → beauti<span class="verb-hi">fy</span> (làm đẹp)<br>
            class → classi<span class="verb-hi">fy</span> (phân loại)
          </div>
        </div>
      </div>
    </div>

    <div class="quiz-box">
      <div class="quiz-title">⚡ Kiểm Tra Nhanh – Động Từ</div>
      <div class="quiz-sci">🔬 Retrieval Practice — tự tìm lại đáp án từ trí nhớ giúp củng cố kết nối neuron (Roediger &amp; Butler, 2011)</div>
      <div class="quiz-question" id="q4">
        <p>1. "beauty" (n) → ______ (v) (làm đẹp)</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q4" data-correct="false" data-msg="beautiness không phải từ tiếng Anh.">beautiness</button>
          <button class="quiz-opt" data-qid="q4" data-correct="true" data-msg="beauty + -fy → beautify ✅">beautify</button>
          <button class="quiz-opt" data-qid="q4" data-correct="false" data-msg="beauten không phải dạng hợp lệ.">beauten</button>
          <button class="quiz-opt" data-qid="q4" data-correct="false" data-msg="-ize thường dùng với tính từ/danh từ khác.">beautize</button>
        </div>
        <div class="quiz-feedback" id="fb-q4"></div>
      </div>
      <div class="quiz-question" id="q5">
        <p>2. "social" (adj) → ______ (v) nghĩa "giao lưu, hòa nhập"</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q5" data-correct="false" data-msg="sociale không phải dạng tiếng Anh.">sociale</button>
          <button class="quiz-opt" data-qid="q5" data-correct="true" data-msg="social + -ize → socialize ✅">socialize</button>
          <button class="quiz-opt" data-qid="q5" data-correct="false" data-msg="socially là trạng từ.">socially</button>
          <button class="quiz-opt" data-qid="q5" data-correct="false" data-msg="sociality là danh từ.">sociality</button>
        </div>
        <div class="quiz-feedback" id="fb-q5"></div>
      </div>
    </div>

    <!-- ════ III. TÍNH TỪ ════ -->
    <div id="tinh-tu" class="subsection-title">III. Cách tạo Tính Từ (Adjective) 🌸</div>
    <div class="phase-chip chip-learn">📘 Pha Học · Đọc hiểu có chọn lọc</div>

    <div class="theory-card">
      <div class="rule-grid">
        <div class="rule-item">
          <div class="rule-formula">N + <span class="adj-hi">-ful</span> → Adj</div>
          <div class="rule-example">
            care → care<span class="adj-hi">ful</span> (cẩn thận)<br>
            success → success<span class="adj-hi">ful</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="adj-hi">-less</span> → Adj</div>
          <div class="rule-example">
            hope → hope<span class="adj-hi">less</span> (vô vọng)<br>
            home → home<span class="adj-hi">less</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="adj-hi">-ous</span> → Adj</div>
          <div class="rule-example">
            danger → danger<span class="adj-hi">ous</span><br>
            industry → industri<span class="adj-hi">ous</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="adj-hi">-al</span> → Adj</div>
          <div class="rule-example">
            nation → nation<span class="adj-hi">al</span><br>
            nature → natur<span class="adj-hi">al</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="adj-hi">-able / -ible</span> → Adj</div>
          <div class="rule-example">
            reason → reason<span class="adj-hi">able</span><br>
            response → respons<span class="adj-hi">ible</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="adj-hi">-ive</span> → Adj</div>
          <div class="rule-example">
            impress → impress<span class="adj-hi">ive</span><br>
            invent → invent<span class="adj-hi">ive</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">V + <span class="adj-hi">-ing / -ed</span> → Adj</div>
          <div class="rule-example">
            interest → interest<span class="adj-hi">ing</span> / interest<span class="adj-hi">ed</span><br>
            bore → bor<span class="adj-hi">ing</span> / bor<span class="adj-hi">ed</span>
          </div>
        </div>
        <div class="rule-item">
          <div class="rule-formula">N + <span class="adj-hi">-y / -ic / -ish</span></div>
          <div class="rule-example">
            rain → rain<span class="adj-hi">y</span> &nbsp;|&nbsp; economy → econom<span class="adj-hi">ic</span><br>
            fool → fool<span class="adj-hi">ish</span>
          </div>
        </div>
      </div>

      <div class="note-box" style="margin-top:18px;">
        <strong>⚠️ Phân biệt -ing vs -ed:</strong><br>
        • <strong>-ing</strong> → mô tả bản chất sự vật: The movie is <strong>boring</strong>. (bộ phim ấy tẻ nhạt)<br>
        • <strong>-ed</strong> → mô tả cảm xúc của người: I am <strong>bored</strong>. (tôi cảm thấy chán)<br>
        → Tương tự: <em>exciting / excited, interesting / interested, disappointing / disappointed</em>…
      </div>
    </div>

    <div class="quiz-box">
      <div class="quiz-title">⚡ Kiểm Tra Nhanh – Tính Từ</div>
      <div class="quiz-sci">🔬 Elaborative Interrogation — não ghi nhớ tốt hơn khi hiểu LÝ DO đúng/sai (Pressley et al., 1992)</div>
      <div class="quiz-question" id="q6">
        <p>1. "The movie was very ______. I fell asleep." (tính chất của phim – chán)</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q6" data-correct="true" data-msg="-ing mô tả bản chất sự vật: The movie was boring ✅">boring</button>
          <button class="quiz-opt" data-qid="q6" data-correct="false" data-msg="-ed mô tả cảm xúc người: I was bored – không mô tả bộ phim.">bored</button>
          <button class="quiz-opt" data-qid="q6" data-correct="false" data-msg="boreness không phải từ tiếng Anh.">boreness</button>
          <button class="quiz-opt" data-qid="q6" data-correct="false" data-msg="boredom là danh từ (sự buồn chán).">boredom</button>
        </div>
        <div class="quiz-feedback" id="fb-q6"></div>
      </div>
      <div class="quiz-question" id="q7">
        <p>2. "danger" (n) → ______ (adj) nghĩa "nguy hiểm"</p>
        <div class="quiz-options">
          <button class="quiz-opt" data-qid="q7" data-correct="false" data-msg="-ful = đầy = dangerous? Không, -ful ≠ đầy nguy hiểm trong TH này.">dangerful</button>
          <button class="quiz-opt" data-qid="q7" data-correct="false" data-msg="-ly tạo trạng từ, không phải tính từ.">dangerly</button>
          <button class="quiz-opt" data-qid="q7" data-correct="true" data-msg="danger + -ous → dangerous ✅ (N + -ous = adj)">dangerous</button>
          <button class="quiz-opt" data-qid="q7" data-correct="false" data-msg="-al thường dùng với từ khác: national, natural.">dangeral</button>
        </div>
        <div class="quiz-feedback" id="fb-q7"></div>
      </div>
    </div>

    <!-- ════ IV. TRẠNG TỪ ════ -->
    <div id="trang-tu" class="subsection-title">IV. Cách tạo Trạng Từ (Adverb) 🌙</div>
    <div class="phase-chip chip-learn">📘 Pha Học · Đọc hiểu có chọn lọc</div>

    <div class="theory-card">
      <div class="rule-item" style="max-width:380px;margin-bottom:16px;">
        <div class="rule-formula">Adj + <span class="adv-hi">-ly</span> → Adv</div>
        <div class="rule-example">
          slow → slow<span class="adv-hi">ly</span> &nbsp;|&nbsp;
          rapid → rapid<span class="adv-hi">ly</span><br>
          careful → careful<span class="adv-hi">ly</span>
        </div>
      </div>
      <div class="note-box">
        <strong>⚠️ Ngoại lệ PHẢI NHỚ:</strong><br>
        🔹 <strong>fast</strong> → vừa adj vừa adv (KHÔNG có "fastly")<br>
        🔹 <strong>hard</strong> (adj/adv = chăm chỉ) ≠ <strong>hardly</strong> (adv = hầu như không)<br>
        🔹 <strong>good</strong> (adj) → <strong>well</strong> (adv) — KHÔNG có "goodly"<br>
        🔹 <strong>-ly</strong> đôi khi là tính từ: <em>friend<strong>ly</strong>, like<strong>ly</strong>, love<strong>ly</strong></em>
      </div>
    </div>

    <!-- ════ V. NHẬN BIẾT TỪ LOẠI THEO VỊ TRÍ ════ -->
    <div id="nhan-biet" class="subsection-title">V. Nhận Biết Từ Loại Qua Ngữ Cảnh 🔍</div>
    <div class="phase-chip chip-learn">📘 Pha Học · Contextual Inference (Nation, 2001)</div>

    <div class="theory-card">
      <p style="font-size:.9rem;color:var(--ink-mid);margin-bottom:16px;">
        Khi gặp ô trống, nhìn vào <strong>các từ xung quanh</strong> để xác định từ loại cần điền.
        Đây là kỹ năng <em>contextual inference</em> — não đọc tín hiệu ngữ cảnh trước khi quyết định.
      </p>
      <table class="ctx-table">
        <thead>
          <tr><th>Dấu hiệu nhận biết</th><th>Từ loại cần điền</th><th>Ví dụ</th></tr>
        </thead>
        <tbody>
          <tr>
            <td><span class="ctx-signal">a / an / the + ___</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>The <strong>development</strong> of science…</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">my / your / his / her / their + ___</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>His <strong>laziness</strong> caused failure.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">Sau giới từ (of / in / on / at)</span></td>
            <td><span class="ctx-pos">Danh từ (N)</span></td>
            <td>30 years of <strong>marriage</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">to be (am/is/are) + ___</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td>The book is <strong>interesting</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">look / seem / feel / become + ___</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td>She looks <strong>happier</strong> today.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">___ + noun (trước danh từ)</span></td>
            <td><span class="ctx-pos">Tính từ (Adj)</span></td>
            <td><strong>Poisonous</strong> snakes are rare.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">Động từ thường + ___</span></td>
            <td><span class="ctx-pos">Trạng từ (Adv)</span></td>
            <td>He runs <strong>quickly</strong>.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">Trước tính từ</span></td>
            <td><span class="ctx-pos">Trạng từ (Adv)</span></td>
            <td>The matter is <strong>comparatively</strong> complex.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">to + ___ (nguyên thể)</span></td>
            <td><span class="ctx-pos">Động từ (V)</span></td>
            <td>We need to <strong>conserve</strong> energy.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">will / can / must / should + ___</span></td>
            <td><span class="ctx-pos">Động từ (V)</span></td>
            <td>You should <strong>develop</strong> this skill.</td>
          </tr>
          <tr>
            <td><span class="ctx-signal">A and/or B → cân bằng</span></td>
            <td><span class="ctx-pos">Cùng từ loại với vế kia</span></td>
            <td>She is <strong>confident</strong> and positive.</td>
          </tr>
        </tbody>
      </table>

      <div class="quiz-box" style="margin-top:20px;">
        <div class="quiz-title">⚡ Thực Hành Nhận Biết</div>
        <div class="quiz-sci">🔬 Contextual Inference — nhận từ loại qua tín hiệu ngữ cảnh (Nation, 2001)</div>
        <div class="quiz-question" id="q8">
          <p>1. "He failed because of his ______" — ô trống cần từ loại gì?</p>
          <div class="quiz-options">
            <button class="quiz-opt" data-qid="q8" data-correct="true" data-msg="Sau &quot;his&quot; (tính từ sở hữu) → cần DANH TỪ: laziness ✅">Danh từ (N)</button>
            <button class="quiz-opt" data-qid="q8" data-correct="false" data-msg="Tính từ đứng trước danh từ hoặc sau to be, không phải sau &quot;his&quot;.">Tính từ (Adj)</button>
            <button class="quiz-opt" data-qid="q8" data-correct="false" data-msg="Trạng từ bổ nghĩa động từ hoặc tính từ, không đứng sau &quot;his&quot;.">Trạng từ (Adv)</button>
            <button class="quiz-opt" data-qid="q8" data-correct="false" data-msg="Động từ không đứng sau tính từ sở hữu.">Động từ (V)</button>
          </div>
          <div class="quiz-feedback" id="fb-q8"></div>
        </div>
        <div class="quiz-question" id="q9">
          <p>2. "The matter is comparatively ______" — ô trống cần từ loại gì?</p>
          <div class="quiz-options">
            <button class="quiz-opt" data-qid="q9" data-correct="false" data-msg="Danh từ không đứng sau to be + trạng từ như vậy.">Danh từ (N)</button>
            <button class="quiz-opt" data-qid="q9" data-correct="true" data-msg="Sau to be + trạng từ (comparatively) → cần TÍNH TỪ ✅">Tính từ (Adj)</button>
            <button class="quiz-opt" data-qid="q9" data-correct="false" data-msg="Đã có trạng từ &quot;comparatively&quot; rồi, không cần thêm.">Trạng từ (Adv)</button>
            <button class="quiz-opt" data-qid="q9" data-correct="false" data-msg="Động từ không đứng sau to be trong ngữ cảnh này.">Động từ (V)</button>
          </div>
          <div class="quiz-feedback" id="fb-q9"></div>
        </div>
      </div>
    </div>
  </section>

  <!-- ══════════════════════════════════
       SƠ ĐỒ TỔNG HỢP
  ══════════════════════════════════ -->
  <section id="so-do">
    <div class="section-title"><span class="icon">🗺</span> Sơ Đồ Tổng Hợp – Word Family Map</div>
    <div class="phase-chip chip-learn">📘 Visual Mapping · Sơ đồ hoá để não nhớ hình ảnh</div>

    <div class="diagram-wrap">
      <svg viewBox="0 0 820 380" xmlns="http://www.w3.org/2000/svg" font-family="Nunito, sans-serif">
        <!-- Center -->
        <rect x="310" y="160" width="200" height="60" rx="30" fill="#4a2c7a" />
        <text x="410" y="186" text-anchor="middle" fill="white" font-size="13" font-weight="900">TỪ GỐC</text>
        <text x="410" y="205" text-anchor="middle" fill="#e8dff7" font-size="12" font-weight="700">ROOT WORD</text>

        <!-- Connector lines -->
        <line x1="310" y1="185" x2="180" y2="90" stroke="#c4aee8" stroke-width="2" stroke-dasharray="5,3"/>
        <line x1="510" y1="185" x2="640" y2="90" stroke="#86efac" stroke-width="2" stroke-dasharray="5,3"/>
        <line x1="310" y1="200" x2="180" y2="300" stroke="#fcd34d" stroke-width="2" stroke-dasharray="5,3"/>
        <line x1="510" y1="200" x2="640" y2="300" stroke="#f9a8d4" stroke-width="2" stroke-dasharray="5,3"/>

        <!-- NOUN card -->
        <rect x="30" y="30" width="220" height="130" rx="14" fill="#dbeafe" stroke="#93c5fd" stroke-width="2"/>
        <text x="140" y="58" text-anchor="middle" fill="#1d4ed8" font-size="11" font-weight="900" letter-spacing="1">📘 DANH TỪ (N)</text>
        <text x="50" y="80" fill="#1e40af" font-size="10.5" font-weight="700">-ment, -ance, -ence, -ion</text>
        <text x="50" y="97" fill="#1e40af" font-size="10.5" font-weight="700">-ation, -al, -age, -ing</text>
        <text x="50" y="114" fill="#1e40af" font-size="10.5" font-weight="700">-er, -or, -ar, -ant, -ee</text>
        <text x="50" y="131" fill="#1e40af" font-size="10.5" font-weight="700">-ist, -ness, -ity, -dom</text>
        <text x="50" y="148" fill="#1e40af" font-size="10.5" font-weight="700">-hood, -ship, -th</text>

        <!-- VERB card -->
        <rect x="570" y="30" width="220" height="115" rx="14" fill="#dcfce7" stroke="#86efac" stroke-width="2"/>
        <text x="680" y="58" text-anchor="middle" fill="#166534" font-size="11" font-weight="900" letter-spacing="1">🌿 ĐỘNG TỪ (V)</text>
        <text x="590" y="80" fill="#166534" font-size="10.5" font-weight="700">Adj + -en → widen</text>
        <text x="590" y="97" fill="#166534" font-size="10.5" font-weight="700">en- + Adj → enrich</text>
        <text x="590" y="114" fill="#166534" font-size="10.5" font-weight="700">-ize / -ise → socialize</text>
        <text x="590" y="131" fill="#166534" font-size="10.5" font-weight="700">-ify / -fy → beautify</text>

        <!-- ADJ card -->
        <rect x="30" y="240" width="220" height="130" rx="14" fill="#fef3c7" stroke="#fcd34d" stroke-width="2"/>
        <text x="140" y="268" text-anchor="middle" fill="#92400e" font-size="11" font-weight="900" letter-spacing="1">🌸 TÍNH TỪ (Adj)</text>
        <text x="50" y="290" fill="#92400e" font-size="10.5" font-weight="700">-ful, -less, -ous, -al</text>
        <text x="50" y="307" fill="#92400e" font-size="10.5" font-weight="700">-able, -ible, -ive</text>
        <text x="50" y="324" fill="#92400e" font-size="10.5" font-weight="700">-ing, -ed, -y, -ic</text>
        <text x="50" y="341" fill="#92400e" font-size="10.5" font-weight="700">-ish, -like, -some</text>
        <text x="50" y="358" fill="#92400e" font-size="10.5" font-weight="700">⚠️ -ing ≠ -ed (nghĩa khác!)</text>

        <!-- ADV card -->
        <rect x="570" y="240" width="220" height="100" rx="14" fill="#fce7f3" stroke="#f9a8d4" stroke-width="2"/>
        <text x="680" y="268" text-anchor="middle" fill="#9d174d" font-size="11" font-weight="900" letter-spacing="1">🌙 TRẠNG TỪ (Adv)</text>
        <text x="590" y="290" fill="#9d174d" font-size="10.5" font-weight="700">Adj + -ly → quickly</text>
        <text x="590" y="307" fill="#9d174d" font-size="10.5" font-weight="700">⚠️ fast / good → well</text>
        <text x="590" y="324" fill="#9d174d" font-size="10.5" font-weight="700">⚠️ hard ≠ hardly</text>
      </svg>
    </div>
  </section>

  <!-- ══════════════════════════════════
       WORD FAMILY TABLE
  ══════════════════════════════════ -->
  <section id="word-family" style="margin-top:20px;">
    <div class="section-title"><span class="icon">🔗</span> Họ Từ Thực Hành (Word Families)</div>
    <div class="phase-chip chip-learn">📘 Semantic Clustering — nhóm từ cùng gốc để não liên kết dễ hơn</div>

    <div class="theory-card">
      <table class="wf-table">
        <thead>
          <tr>
            <th>Từ gốc</th>
            <th><span class="pos-chip pos-n">N</span> Danh từ</th>
            <th><span class="pos-chip pos-v">V</span> Động từ</th>
            <th><span class="pos-chip pos-a">Adj</span> Tính từ</th>
            <th><span class="pos-chip pos-adv">Adv</span> Trạng từ</th>
          </tr>
        </thead>
        <tbody>
          <tr>
            <td class="wf-root">beauty</td>
            <td>beau<strong>ty</strong></td>
            <td>beauti<strong>fy</strong></td>
            <td>beauti<strong>ful</strong></td>
            <td>beauti<strong>fully</strong></td>
          </tr>
          <tr>
            <td class="wf-root">develop</td>
            <td>develop<strong>ment</strong></td>
            <td>develop</td>
            <td>develop<strong>ed</strong> / develop<strong>ing</strong></td>
            <td>—</td>
          </tr>
          <tr>
            <td class="wf-root">danger</td>
            <td>danger</td>
            <td>endanger</td>
            <td>danger<strong>ous</strong></td>
            <td>danger<strong>ously</strong></td>
          </tr>
          <tr>
            <td class="wf-root">success</td>
            <td>success</td>
            <td>succeed</td>
            <td>success<strong>ful</strong></td>
            <td>success<strong>fully</strong></td>
          </tr>
          <tr>
            <td class="wf-root">nation</td>
            <td>nation / nation<strong>ality</strong></td>
            <td>national<strong>ize</strong></td>
            <td>nation<strong>al</strong></td>
            <td>nation<strong>ally</strong></td>
          </tr>
          <tr>
            <td class="wf-root">care</td>
            <td>care</td>
            <td>care</td>
            <td>care<strong>ful</strong> / care<strong>less</strong></td>
            <td>care<strong>fully</strong> / care<strong>lessly</strong></td>
          </tr>
          <tr>
            <td class="wf-root">invent</td>
            <td>invent<strong>ion</strong> / invent<strong>or</strong></td>
            <td>invent</td>
            <td>invent<strong>ive</strong></td>
            <td>invent<strong>ively</strong></td>
          </tr>
          <tr>
            <td class="wf-root">employ</td>
            <td>employ<strong>er</strong> / employ<strong>ee</strong> / employ<strong>ment</strong></td>
            <td>employ</td>
            <td>employ<strong>able</strong></td>
            <td>—</td>
          </tr>
        </tbody>
      </table>
    </div>
  </section>

  <!-- ══════════════════════════════════
       GIAI ĐOẠN 2 – GỢI NHỚ CHỦ ĐỘNG
  ══════════════════════════════════ -->
  <section id="goi-nho">
    <div class="section-title"><span class="icon">🧠</span> Giai Đoạn 2 – Ôn Tập Gợi Nhớ Chủ Động</div>

    <div class="note-box">
      <strong>🔬 Tại sao phải GỢI NHỚ thay vì đọc lại?</strong><br>
      Nghiên cứu của Roediger &amp; Butler (2011) cho thấy: tự <em>cố lấy lại</em> thông tin từ trí nhớ (retrieval practice) giúp nhớ lâu hơn 50% so với đọc lại tài liệu. Dưới đây, em sẽ tự điền vào ô trống mà không nhìn lý thuyết.
    </div>

    <!-- Recall set 1: Hậu tố -->
    <div class="recall-box">
      <div class="recall-title">🔁 Thử Thách Gợi Nhớ – Hậu Tố</div>
      <div class="recall-sci">🔬 Retrieval Practice · Tự tái tạo thông tin không nhìn gợi ý (Roediger &amp; Butler, 2011)</div>

      <div class="recall-item">
        <div class="recall-q">1. "attend" (v) → ______ (n) · <em>nhớ hậu tố chỉ hành động/trạng thái</em></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r1" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r1',['attendance'],'attendance (-ance)')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h1','Gợi ý: attend + -ance')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h1"></div>
        <div class="quiz-feedback" id="fb-r1"></div>
      </div>

      <div class="recall-item">
        <div class="recall-q">2. "invent" (v) → ______ (n) · <em>nhớ hậu tố tạo danh từ từ hành động</em></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r2" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r2',['invention'],'invention (-ion)')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h2','Gợi ý: invent + -ion')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h2"></div>
        <div class="quiz-feedback" id="fb-r2"></div>
      </div>

      <div class="recall-item">
        <div class="recall-q">3. "wide" (adj) → ______ (v) · <em>nhớ hậu tố biến adj thành động từ</em></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r3" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r3',['widen'],'widen (wide + -en)')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h3','Gợi ý: wide + -en')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h3"></div>
        <div class="quiz-feedback" id="fb-r3"></div>
      </div>

      <div class="recall-item">
        <div class="recall-q">4. "hope" (n) → ______ (adj) · <em>tính từ nghĩa "vô vọng"</em></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r4" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r4',['hopeless'],'hopeless (hope + -less)')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h4','Gợi ý: hope + -less')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h4"></div>
        <div class="quiz-feedback" id="fb-r4"></div>
      </div>

      <div class="recall-item">
        <div class="recall-q">5. "rapid" (adj) → ______ (adv) · <em>nhớ hậu tố tạo trạng từ</em></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r5" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r5',['rapidly'],'rapidly (rapid + -ly)')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h5','Gợi ý: rapid + -ly')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h5"></div>
        <div class="quiz-feedback" id="fb-r5"></div>
      </div>
    </div>

    <!-- Recall set 2: Nhận diện ngữ cảnh -->
    <div class="recall-box">
      <div class="recall-title">🔁 Thử Thách Gợi Nhớ – Nhận Diện Ngữ Cảnh</div>
      <div class="recall-sci">🔬 Contextual Inference · Tự suy luận từ loại qua tín hiệu câu (Nation, 2001)</div>

      <div class="recall-item">
        <div class="recall-q">6. "Her ______ surprised everyone." → "friend" (n) cần biến thành dạng nào?<br>
        <small style="color:var(--ink-light)">(Gợi ý: sau "her" → từ loại gì?)</small></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r6" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r6',['friendliness','friendliness','kindness'],'friendliness (friendly + -ness = danh từ, sau "her")')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h6','Gợi ý: her + N → friendly → friendliness')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h6"></div>
        <div class="quiz-feedback" id="fb-r6"></div>
      </div>

      <div class="recall-item">
        <div class="recall-q">7. "Scientists must ______ new solutions." → "invent" cần dạng nào?<br>
        <small style="color:var(--ink-light)">(Gợi ý: sau "must" → từ loại gì?)</small></div>
        <div class="recall-input-row">
          <input class="recall-input" id="r7" type="text" placeholder="điền vào đây…" autocomplete="off" />
          <button class="recall-check" onclick="checkRecall('r7',['invent'],'invent – sau modal (must) → V nguyên dạng ✅')">Kiểm tra</button>
          <button class="reveal-btn" onclick="revealHint('h7','Gợi ý: must + V nguyên dạng')">💡 Gợi ý</button>
        </div>
        <div class="recall-hint" id="h7"></div>
        <div class="quiz-feedback" id="fb-r7"></div>
      </div>
    </div>
  </section>

  <!-- ══════════════════════════════════
       GIAI ĐOẠN 3 – BÀI TẬP ÁP DỤNG
  ══════════════════════════════════ -->
  <section id="bai-tap">
    <div class="section-title"><span class="icon">✏️</span> Giai Đoạn 3 – Bài Tập Ứng Dụng</div>

    <!-- Exercise 1 -->
    <div class="exercise-wrap">
      <div class="exercise-head">
        <span style="font-size:1.4rem;">📝</span>
        <h3>Bài Tập 1 – Nhận Diện Từ Loại (10 câu)</h3>
        <span class="sci-badge">⚡ Retrieval Practice</span>
      </div>
      <div class="exercise-body">
        <p style="font-size:.88rem;color:var(--ink-light);margin-bottom:20px;font-weight:700;">
          Chọn từ đúng để điền vào ô trống dựa trên ngữ cảnh câu.
        </p>

        <!-- Q1 -->
        <div class="ex-q"><div class="ex-num">1</div><div class="ex-content">
          <div class="ex-sentence">The ______ of the internet has changed how we learn.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-1" data-correct="true" data-msg="✅ Sau &quot;the&quot; → danh từ: development">development</button>
            <button class="ex-opt" data-exid="e1-1" data-correct="false" data-msg="develop là động từ, không đứng sau mạo từ &quot;the&quot;.">develop</button>
            <button class="ex-opt" data-exid="e1-1" data-correct="false" data-msg="developed là động từ chia, không phải danh từ.">developed</button>
            <button class="ex-opt" data-exid="e1-1" data-correct="false" data-msg="developing là adj/v-ing, không phải danh từ chỉ kết quả.">developing</button>
          </div>
          <div class="ex-fb" id="fb-e1-1"></div>
        </div></div>

        <!-- Q2 -->
        <div class="ex-q"><div class="ex-num">2</div><div class="ex-content">
          <div class="ex-sentence">She spoke ______ in front of the whole class.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-2" data-correct="false" data-msg="confidence là danh từ, không bổ nghĩa động từ.">confidence</button>
            <button class="ex-opt" data-exid="e1-2" data-correct="false" data-msg="confident là tính từ, không bổ nghĩa động từ spoke.">confident</button>
            <button class="ex-opt" data-exid="e1-2" data-correct="true" data-msg="✅ Sau động từ &quot;spoke&quot; → trạng từ: confidently">confidently</button>
            <button class="ex-opt" data-exid="e1-2" data-correct="false" data-msg="confide là động từ, không bổ nghĩa động từ.">confide</button>
          </div>
          <div class="ex-fb" id="fb-e1-2"></div>
        </div></div>

        <!-- Q3 -->
        <div class="ex-q"><div class="ex-num">3</div><div class="ex-content">
          <div class="ex-sentence">Air pollution is a very ______ problem in big cities.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-3" data-correct="false" data-msg="seriously là trạng từ.">seriously</button>
            <button class="ex-opt" data-exid="e1-3" data-correct="true" data-msg="✅ Trước danh từ &quot;problem&quot; → tính từ: serious">serious</button>
            <button class="ex-opt" data-exid="e1-3" data-correct="false" data-msg="seriousness là danh từ.">seriousness</button>
            <button class="ex-opt" data-exid="e1-3" data-correct="false" data-msg="seriousify không phải từ tiếng Anh.">seriousify</button>
          </div>
          <div class="ex-fb" id="fb-e1-3"></div>
        </div></div>

        <!-- Q4 -->
        <div class="ex-q"><div class="ex-num">4</div><div class="ex-content">
          <div class="ex-sentence">We need to ______ our vocabulary every day.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-4" data-correct="false" data-msg="enrichment là danh từ.">enrichment</button>
            <button class="ex-opt" data-exid="e1-4" data-correct="false" data-msg="enriched là quá khứ, không theo sau &quot;to&quot;.">enriched</button>
            <button class="ex-opt" data-exid="e1-4" data-correct="true" data-msg="✅ Sau &quot;to&quot; nguyên thể → V nguyên dạng: enrich">enrich</button>
            <button class="ex-opt" data-exid="e1-4" data-correct="false" data-msg="enriching là V-ing, không dùng sau &quot;to&quot;.">enriching</button>
          </div>
          <div class="ex-fb" id="fb-e1-4"></div>
        </div></div>

        <!-- Q5 -->
        <div class="ex-q"><div class="ex-num">5</div><div class="ex-content">
          <div class="ex-sentence">His ______ at school made his parents proud.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-5" data-correct="true" data-msg="✅ Sau &quot;his&quot; → danh từ: achievement">achievement</button>
            <button class="ex-opt" data-exid="e1-5" data-correct="false" data-msg="achieve là động từ, không đứng sau &quot;his&quot;.">achieve</button>
            <button class="ex-opt" data-exid="e1-5" data-correct="false" data-msg="achievable là tính từ, không đứng sau &quot;his&quot;.">achievable</button>
            <button class="ex-opt" data-exid="e1-5" data-correct="false" data-msg="achievably là trạng từ.">achievably</button>
          </div>
          <div class="ex-fb" id="fb-e1-5"></div>
        </div></div>

        <!-- Q6 -->
        <div class="ex-q"><div class="ex-num">6</div><div class="ex-content">
          <div class="ex-sentence">The teacher looks ______ with today's results.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-6" data-correct="false" data-msg="satisfaction là danh từ, không đứng sau &quot;looks&quot;.">satisfaction</button>
            <button class="ex-opt" data-exid="e1-6" data-correct="false" data-msg="satisfactorily là trạng từ.">satisfactorily</button>
            <button class="ex-opt" data-exid="e1-6" data-correct="false" data-msg="satisfy là động từ, không đứng sau &quot;looks&quot;.">satisfy</button>
            <button class="ex-opt" data-exid="e1-6" data-correct="true" data-msg="✅ Sau &quot;looks&quot; (linking verb) → tính từ: satisfied">satisfied</button>
          </div>
          <div class="ex-fb" id="fb-e1-6"></div>
        </div></div>

        <!-- Q7 -->
        <div class="ex-q"><div class="ex-num">7</div><div class="ex-content">
          <div class="ex-sentence">Reading is an ______ hobby for students.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-7" data-correct="true" data-msg="✅ Trước danh từ &quot;hobby&quot; → tính từ: enjoyable">enjoyable</button>
            <button class="ex-opt" data-exid="e1-7" data-correct="false" data-msg="enjoyment là danh từ.">enjoyment</button>
            <button class="ex-opt" data-exid="e1-7" data-correct="false" data-msg="enjoy là động từ, không đứng trước danh từ như adj.">enjoy</button>
            <button class="ex-opt" data-exid="e1-7" data-correct="false" data-msg="enjoyably là trạng từ.">enjoyably</button>
          </div>
          <div class="ex-fb" id="fb-e1-7"></div>
        </div></div>

        <!-- Q8 -->
        <div class="ex-q"><div class="ex-num">8</div><div class="ex-content">
          <div class="ex-sentence">The government should ______ transportation in rural areas.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-8" data-correct="false" data-msg="improvement là danh từ, không đứng sau &quot;should&quot;.">improvement</button>
            <button class="ex-opt" data-exid="e1-8" data-correct="true" data-msg="✅ Sau modal &quot;should&quot; → V nguyên dạng: improve">improve</button>
            <button class="ex-opt" data-exid="e1-8" data-correct="false" data-msg="improved là quá khứ/V-ed, không dùng sau modal.">improved</button>
            <button class="ex-opt" data-exid="e1-8" data-correct="false" data-msg="improving là V-ing, không dùng sau modal.">improving</button>
          </div>
          <div class="ex-fb" id="fb-e1-8"></div>
        </div></div>

        <!-- Q9 -->
        <div class="ex-q"><div class="ex-num">9</div><div class="ex-content">
          <div class="ex-sentence">Pollution is becoming an ______ serious issue worldwide.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-9" data-correct="false" data-msg="increase là động từ/danh từ, không bổ nghĩa tính từ.">increase</button>
            <button class="ex-opt" data-exid="e1-9" data-correct="false" data-msg="increased là adj nhưng không bổ nghĩa tính từ.">increased</button>
            <button class="ex-opt" data-exid="e1-9" data-correct="true" data-msg="✅ Trước tính từ &quot;serious&quot; → trạng từ: increasingly">increasingly</button>
            <button class="ex-opt" data-exid="e1-9" data-correct="false" data-msg="increasing là adj/v-ing, không bổ nghĩa tính từ.">increasing</button>
          </div>
          <div class="ex-fb" id="fb-e1-9"></div>
        </div></div>

        <!-- Q10 -->
        <div class="ex-q"><div class="ex-num">10</div><div class="ex-content">
          <div class="ex-sentence">The ______ of mobile phones has transformed modern life.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e1-10" data-correct="false" data-msg="invent là động từ, không đứng sau &quot;the&quot;.">invent</button>
            <button class="ex-opt" data-exid="e1-10" data-correct="false" data-msg="inventive là tính từ.">inventive</button>
            <button class="ex-opt" data-exid="e1-10" data-correct="true" data-msg="✅ Sau &quot;the&quot; → danh từ: invention">invention</button>
            <button class="ex-opt" data-exid="e1-10" data-correct="false" data-msg="inventively là trạng từ.">inventively</button>
          </div>
          <div class="ex-fb" id="fb-e1-10"></div>
        </div></div>

        <div class="score-bar" id="sb1" style="display:none">
          <div>
            <div class="score-num" id="sn1">0/10</div>
            <div class="score-label">điểm Bài 1</div>
          </div>
          <div class="score-msg" id="sm1"></div>
        </div>
      </div>
    </div>

    <!-- Exercise 2 -->
    <div class="exercise-wrap">
      <div class="exercise-head">
        <span style="font-size:1.4rem;">📝</span>
        <h3>Bài Tập 2 – Ứng Dụng Tổng Hợp (10 câu)</h3>
        <span class="sci-badge">⚡ Elaborative Interrogation</span>
      </div>
      <div class="exercise-body">
        <p style="font-size:.88rem;color:var(--ink-light);margin-bottom:20px;font-weight:700;">
          Chọn dạng từ đúng. Mỗi câu có giải thích chi tiết khi trả lời.
        </p>

        <!-- Q1 -->
        <div class="ex-q"><div class="ex-num">1</div><div class="ex-content">
          <div class="ex-sentence">She showed great ______ during the difficult exam.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-1" data-correct="true" data-msg="✅ Sau &quot;great&quot; → danh từ: determination (sự quyết tâm)">determination</button>
            <button class="ex-opt" data-exid="e2-1" data-correct="false" data-msg="determine là động từ.">determine</button>
            <button class="ex-opt" data-exid="e2-1" data-correct="false" data-msg="determined là tính từ/quá khứ.">determined</button>
            <button class="ex-opt" data-exid="e2-1" data-correct="false" data-msg="determinedly là trạng từ.">determinedly</button>
          </div>
          <div class="ex-fb" id="fb-e2-1"></div>
        </div></div>

        <!-- Q2 -->
        <div class="ex-q"><div class="ex-num">2</div><div class="ex-content">
          <div class="ex-sentence">The children were ______ by the magic show.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-2" data-correct="false" data-msg="amazement là danh từ.">amazement</button>
            <button class="ex-opt" data-exid="e2-2" data-correct="false" data-msg="amazing mô tả bản chất sự vật (show was amazing), không phải cảm xúc của người.">amazing</button>
            <button class="ex-opt" data-exid="e2-2" data-correct="true" data-msg="✅ Cảm xúc của trẻ em → -ed: amazed ✅">amazed</button>
            <button class="ex-opt" data-exid="e2-2" data-correct="false" data-msg="amaze là động từ nguyên dạng.">amaze</button>
          </div>
          <div class="ex-fb" id="fb-e2-2"></div>
        </div></div>

        <!-- Q3 -->
        <div class="ex-q"><div class="ex-num">3</div><div class="ex-content">
          <div class="ex-sentence">Learning a new language requires a lot of ______.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-3" data-correct="false" data-msg="persistent là tính từ.">persistent</button>
            <button class="ex-opt" data-exid="e2-3" data-correct="false" data-msg="persist là động từ.">persist</button>
            <button class="ex-opt" data-exid="e2-3" data-correct="false" data-msg="persistently là trạng từ.">persistently</button>
            <button class="ex-opt" data-exid="e2-3" data-correct="true" data-msg="✅ Sau &quot;of&quot; (giới từ) → danh từ: persistence">persistence</button>
          </div>
          <div class="ex-fb" id="fb-e2-3"></div>
        </div></div>

        <!-- Q4 -->
        <div class="ex-q"><div class="ex-num">4</div><div class="ex-content">
          <div class="ex-sentence">It is ______ to waste food when many people go hungry.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-4" data-correct="true" data-msg="✅ Sau &quot;is&quot; → tính từ: unacceptable">unacceptable</button>
            <button class="ex-opt" data-exid="e2-4" data-correct="false" data-msg="unacceptably là trạng từ.">unacceptably</button>
            <button class="ex-opt" data-exid="e2-4" data-correct="false" data-msg="unacceptance không phải từ hợp lệ.">unacceptance</button>
            <button class="ex-opt" data-exid="e2-4" data-correct="false" data-msg="accept là động từ nguyên dạng.">accept</button>
          </div>
          <div class="ex-fb" id="fb-e2-4"></div>
        </div></div>

        <!-- Q5 -->
        <div class="ex-q"><div class="ex-num">5</div><div class="ex-content">
          <div class="ex-sentence">The school hopes to ______ its students' digital skills.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-5" data-correct="false" data-msg="strengthening là V-ing, không dùng sau &quot;to&quot; infinitive.">strengthening</button>
            <button class="ex-opt" data-exid="e2-5" data-correct="true" data-msg="✅ Sau &quot;to&quot; nguyên thể → V: strengthen">strengthen</button>
            <button class="ex-opt" data-exid="e2-5" data-correct="false" data-msg="strength là danh từ.">strength</button>
            <button class="ex-opt" data-exid="e2-5" data-correct="false" data-msg="strengthened là quá khứ.">strengthened</button>
          </div>
          <div class="ex-fb" id="fb-e2-5"></div>
        </div></div>

        <!-- Q6 -->
        <div class="ex-q"><div class="ex-num">6</div><div class="ex-content">
          <div class="ex-sentence">His ______ to help others is truly inspiring.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-6" data-correct="true" data-msg="✅ Sau &quot;his&quot; → danh từ: willingness">willingness</button>
            <button class="ex-opt" data-exid="e2-6" data-correct="false" data-msg="willing là tính từ.">willing</button>
            <button class="ex-opt" data-exid="e2-6" data-correct="false" data-msg="willingly là trạng từ.">willingly</button>
            <button class="ex-opt" data-exid="e2-6" data-correct="false" data-msg="will là động từ/danh từ nhưng nghĩa khác.">will</button>
          </div>
          <div class="ex-fb" id="fb-e2-6"></div>
        </div></div>

        <!-- Q7 -->
        <div class="ex-q"><div class="ex-num">7</div><div class="ex-content">
          <div class="ex-sentence">This museum contains many ______ artifacts from ancient times.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-7" data-correct="false" data-msg="history là danh từ, không đứng trước danh từ khác.">history</button>
            <button class="ex-opt" data-exid="e2-7" data-correct="false" data-msg="historically là trạng từ.">historically</button>
            <button class="ex-opt" data-exid="e2-7" data-correct="true" data-msg="✅ Trước danh từ &quot;artifacts&quot; → tính từ: historical">historical</button>
            <button class="ex-opt" data-exid="e2-7" data-correct="false" data-msg="historize không phải từ hợp lệ.">historize</button>
          </div>
          <div class="ex-fb" id="fb-e2-7"></div>
        </div></div>

        <!-- Q8 -->
        <div class="ex-q"><div class="ex-num">8</div><div class="ex-content">
          <div class="ex-sentence">The ______ of technology in education has many benefits.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-8" data-correct="false" data-msg="integrate là động từ.">integrate</button>
            <button class="ex-opt" data-exid="e2-8" data-correct="false" data-msg="integrated là tính từ/quá khứ.">integrated</button>
            <button class="ex-opt" data-exid="e2-8" data-correct="true" data-msg="✅ Sau &quot;The&quot; → danh từ: integration">integration</button>
            <button class="ex-opt" data-exid="e2-8" data-correct="false" data-msg="integratively là trạng từ.">integratively</button>
          </div>
          <div class="ex-fb" id="fb-e2-8"></div>
        </div></div>

        <!-- Q9 -->
        <div class="ex-q"><div class="ex-num">9</div><div class="ex-content">
          <div class="ex-sentence">Students should be ______ and ask questions in class.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-9" data-correct="false" data-msg="activeness không phải dạng phổ biến.">activeness</button>
            <button class="ex-opt" data-exid="e2-9" data-correct="false" data-msg="actively là trạng từ.">actively</button>
            <button class="ex-opt" data-exid="e2-9" data-correct="true" data-msg="✅ Sau &quot;be&quot; → tính từ: active">active</button>
            <button class="ex-opt" data-exid="e2-9" data-correct="false" data-msg="activate là động từ.">activate</button>
          </div>
          <div class="ex-fb" id="fb-e2-9"></div>
        </div></div>

        <!-- Q10 -->
        <div class="ex-q"><div class="ex-num">10</div><div class="ex-content">
          <div class="ex-sentence">The factory workers protested against the ______ conditions.</div>
          <div class="ex-opts">
            <button class="ex-opt" data-exid="e2-10" data-correct="false" data-msg="work là danh từ/động từ, đứng trước noun cần là adj.">work</button>
            <button class="ex-opt" data-exid="e2-10" data-correct="false" data-msg="workfully không phải từ hợp lệ.">workfully</button>
            <button class="ex-opt" data-exid="e2-10" data-correct="true" data-msg="✅ Trước &quot;conditions&quot; → tính từ: working">working</button>
            <button class="ex-opt" data-exid="e2-10" data-correct="false" data-msg="worked là quá khứ, không đúng vị trí này.">worked</button>
          </div>
          <div class="ex-fb" id="fb-e2-10"></div>
        </div></div>

        <div class="score-bar" id="sb2" style="display:none">
          <div>
            <div class="score-num" id="sn2">0/10</div>
            <div class="score-label">điểm Bài 2</div>
          </div>
          <div class="score-msg" id="sm2"></div>
        </div>
      </div>
    </div>

    <!-- TOTAL -->
    <div class="total-score-box" id="total-box">
      <div style="font-size:2.4rem;margin-bottom:8px;" id="total-emoji">🏆</div>
      <div style="font-size:2rem;font-weight:900;" id="total-num">–/20</div>
      <div style="opacity:.85;font-size:.95rem;margin-top:4px;">Tổng điểm hai bài tập</div>
      <div style="margin-top:12px;font-size:1rem;font-weight:700;opacity:.9;" id="total-msg"></div>
    </div>
  </section>

</main>

<!-- ═══ FOOTER ═══ -->
<footer class="footer">
  <div class="footer-deco">📚 ✏️ 📖 🔖 📝</div>
  <div style="font-weight:800;margin-bottom:6px;font-size:1rem;">Word Forms – Cấu Tạo Từ</div>
  <div style="opacity:.65;font-size:.82rem;line-height:1.8;">
    Thiết kế dựa trên: Bower et al. (1969) · Slamecka &amp; Graf (1978) · Nation (2001) · Roediger &amp; Butler (2011)<br>
    Tiếng Anh · Học sinh cấp 2 &amp; 3
  </div>
</footer>

<script>
/* ── NAV ACTIVE ── */
document.querySelectorAll('.nav-pill').forEach(p => {
  p.addEventListener('click', function() {
    document.querySelectorAll('.nav-pill').forEach(x => x.classList.remove('active'));
    this.classList.add('active');
  });
});
window.addEventListener('scroll', () => {
  let cur = '';
  document.querySelectorAll('section[id]').forEach(s => {
    if (s.getBoundingClientRect().top < 130) cur = s.id;
  });
  document.querySelectorAll('.nav-pill').forEach(p => {
    p.classList.remove('active');
    if (p.getAttribute('href') === '#' + cur) p.classList.add('active');
  });
});

/* ── QUICK QUIZ ── */
document.addEventListener('DOMContentLoaded', function() {
  // Quiz opts
  document.querySelectorAll('.quiz-opt').forEach(function(btn) {
    btn.addEventListener('click', function() {
      var qid = btn.dataset.qid;
      var correct = btn.dataset.correct === 'true';
      var msg = btn.dataset.msg || '';
      var container = document.getElementById(qid);
      if (!container || container.dataset.done) return;
      container.dataset.done = '1';
      container.querySelectorAll('.quiz-opt').forEach(function(b) {
        b.disabled = true;
        if (b.dataset.correct === 'true') b.classList.add('correct');
      });
      if (!correct) btn.classList.add('wrong');
      var fb = document.getElementById('fb-' + qid);
      if (fb) {
        fb.textContent = correct ? '✅ ' + msg : '❌ ' + msg;
        fb.className = 'quiz-feedback show ' + (correct ? 'ok' : 'err');
      }
    });
  });

  // Ex opts
  document.querySelectorAll('.ex-opt').forEach(function(btn) {
    btn.addEventListener('click', function() {
      var exid = btn.dataset.exid;
      var correct = btn.dataset.correct === 'true';
      var msg = btn.dataset.msg || '';
      if (!exid || answered[exid]) return;
      answered[exid] = true;
      var content = btn.closest('.ex-content');
      content.querySelectorAll('.ex-opt').forEach(function(b) {
        b.disabled = true;
        if (b.dataset.correct === 'true') b.classList.add('correct');
      });
      if (!correct) btn.classList.add('wrong');
      var fb = document.getElementById('fb-' + exid);
      if (fb) {
        fb.textContent = correct ? msg : '❌ ' + msg;
        fb.className = 'ex-fb show ' + (correct ? 'ok' : 'err');
      }
      if (correct) {
        var key = exid.startsWith('e1') ? 'e1' : 'e2';
        scores[key]++;
      }
      updateScore(exid.startsWith('e1') ? 'e1' : 'e2');
    });
  });
});

/* ── RECALL ── */
const recallAnswered = {};
function checkRecall(id, answers, explanation) {
  if (recallAnswered[id]) return;
  const input = document.getElementById(id);
  const val = input.value.trim().toLowerCase();
  const ok = answers.some(a => a.toLowerCase() === val || val === a.toLowerCase().replace(/[^a-z]/g,''));
  recallAnswered[id] = true;
  input.classList.add(ok ? 'ok' : 'err');
  input.disabled = true;
  const fb = document.getElementById('fb-' + id);
  fb.textContent = ok ? '✅ Đúng rồi! ' + explanation : '❌ Chưa đúng. Đáp án: ' + explanation;
  fb.className = 'quiz-feedback show ' + (ok ? 'ok' : 'err');
}
function revealHint(hid, text) {
  const el = document.getElementById(hid);
  el.textContent = text;
  el.className = 'recall-hint show';
}

/* ── EXERCISES ── */
const scores = { e1: 0, e2: 0 };
const answered = {};

function updateScore(key) {
  const prefix = key + '-';
  let done = 0;
  for (let i = 1; i <= 10; i++) if (answered[prefix + i]) done++;
  const n = scores[key];
  const idx = key === 'e1' ? '1' : '2';
  const bar = document.getElementById('sb' + idx);
  if (done === 10) {
    bar.style.display = 'flex';
    document.getElementById('sn' + idx).textContent = n + '/10';
    const msgs = ['💪 Cần ôn thêm! Đọc lại lý thuyết và thử lại.', '👍 Khá tốt! Ôn lại những câu sai.', '⭐ Rất tốt! Tiếp tục phát huy nhé.', '🏆 Xuất sắc! Em đã nắm vững phần này!'];
    const mi = n <= 5 ? 0 : n <= 7 ? 1 : n <= 9 ? 2 : 3;
    document.getElementById('sm' + idx).textContent = msgs[mi];

    const d1 = Array.from({length:10},(_,i)=>answered['e1-'+(i+1)]).every(Boolean);
    const d2 = Array.from({length:10},(_,i)=>answered['e2-'+(i+1)]).every(Boolean);
    if (d1 && d2) {
      const tot = scores.e1 + scores.e2;
      const box = document.getElementById('total-box');
      box.style.display = 'block';
      document.getElementById('total-num').textContent = tot + '/20';
      const emoji = tot >= 18 ? '🏆' : tot >= 14 ? '⭐' : tot >= 10 ? '👍' : '💪';
      document.getElementById('total-emoji').textContent = emoji;
      const tm = tot >= 18 ? 'Tuyệt vời! Em đã nắm vững Word Forms!' :
                 tot >= 14 ? 'Rất tốt! Xem lại những câu sai và ôn lại sơ đồ.' :
                 tot >= 10 ? 'Khá! Ôn lại bảng nhận biết từ loại theo vị trí.' :
                             'Hãy xem lại toàn bộ lý thuyết, sau đó thử lại nhé.';
      document.getElementById('total-msg').textContent = tm;
      box.scrollIntoView({ behavior: 'smooth', block: 'center' });
    }
  }
}
</script>
</body>
</html>
