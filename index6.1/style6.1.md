:root {
  --ink: #20243a;
  --muted: #686e84;
  --purple: #6558d9;
  --purple-soft: #efedff;
  --teal: #bdeee2;
  --orange: #ffd5a8;
  --rose: #f8c7d4;
  --surface: #ffffff;
  --background: #f7f8fc;
  --line: #e5e7f0;
  --shadow: 0 14px 36px rgba(38, 40, 78, .08);
}
* { box-sizing: border-box; }
body { margin: 0; font-family: "Segoe UI", Arial, sans-serif; background: var(--background); color: var(--ink); line-height: 1.65; }
h1, h2, p { margin-top: 0; }
h1, h2 { line-height: 1.15; letter-spacing: -.035em; }
h1 { font-size: clamp(2.2rem, 5vw, 3.6rem); margin-bottom: 14px; }
h1 span { color: var(--purple); }
h2 { font-size: 1.35rem; margin-bottom: 12px; }
p { color: var(--muted); }
.container { width: min(1120px, calc(100% - 36px)); margin: 0 auto; }
.site-header { padding: 54px 0 48px; background: radial-gradient(circle at 85% 20%, #e6e2ff 0, transparent 28%), #fff; border-bottom: 1px solid var(--line); }
.eyebrow { color: var(--purple); font-size: .72rem; font-weight: 850; letter-spacing: .15em; margin-bottom: 10px; }
.intro { max-width: 690px; margin-bottom: 0; font-size: 1.05rem; }
.controls-panel { display: flex; justify-content: space-between; align-items: center; flex-wrap: wrap; gap: 18px; padding: 24px; margin: 30px 0; border: 1px solid var(--line); border-radius: 20px; background: var(--surface); box-shadow: var(--shadow); }
.controls-panel h2 { margin-bottom: 6px; }
.controls-panel p:not(.eyebrow) { margin-bottom: 0; }
.toggle-group { display: flex; padding: 5px; border-radius: 13px; background: #f0f1f8; gap: 4px; }
.mode-button { padding: 10px 14px; border: 0; border-radius: 9px; background: transparent; color: var(--muted); font: inherit; font-size: .88rem; font-weight: 750; cursor: pointer; }
.mode-button.active { color: white; background: var(--purple); box-shadow: 0 5px 12px #6558d933; }
.mode-button:focus-visible { outline: 3px solid #b8b2ff; outline-offset: 2px; }
.mode-note { flex-basis: 100%; font-size: .9rem; }
.cards-grid { display: grid; grid-template-columns: repeat(3, 1fr); align-items: start; gap: 22px; margin-bottom: 32px; }
.demo-card { width: 260px; max-width: 100%; background: white; border-radius: 13px; transition: width .2s, box-shadow .2s; }
.card-one { padding: 12px; border: 2px solid #6558d9; margin: 10px 0 24px; background: #fbfaff; }
.card-two { padding: 24px; border: 5px solid #e6a04f; margin: 24px 0 10px; background: #fffaf4; }
.card-three { padding: 32px; border: 8px solid #40a991; margin: 16px 0 34px; background: #f3fffb; }
.card-number { display: inline-block; padding: 4px 8px; margin-bottom: 13px; border-radius: 7px; background: var(--purple-soft); color: var(--purple); font-size: .7rem; font-weight: 850; letter-spacing: .1em; }
.demo-card h2 { margin-bottom: 9px; }
.demo-card p { font-size: .9rem; margin-bottom: 16px; }
.measure { padding-top: 12px; border-top: 1px solid #dfe0eb; color: var(--muted); font-size: .74rem; font-weight: 700; }
body.border-box-mode .demo-card { box-sizing: border-box; }
body.content-box-mode .demo-card { box-sizing: content-box; }
.explain-grid { display: grid; grid-template-columns: 1.1fr .9fr; gap: 22px; margin-bottom: 32px; }
.explain-card { padding: 27px; border: 1px solid var(--line); border-radius: 20px; background: white; box-shadow: var(--shadow); min-width: 0; }
.explain-card > p { font-size: .92rem; }
.box-model { padding: 16px; margin: 20px 0; border-radius: 14px; background: #f7f8fc; }
.layer { display: flex; align-items: center; justify-content: center; text-align: center; font-size: .68rem; font-weight: 850; letter-spacing: .08em; }
.margin-layer { min-height: 190px; padding: 17px; background: #ffe0e6; color: #8d354b; }
.border-layer { width: 100%; min-height: 150px; padding: 15px; background: #f7bd81; color: #784312; }
.padding-layer { width: 100%; min-height: 112px; padding: 15px; background: #c8c4ff; color: #3d329c; }
.content-layer { display: grid; place-items: center; width: 100%; min-height: 65px; background: #bdeee2; color: #155f50; }
.layer-label { align-self: flex-start; margin-right: 8px; }
.legend { list-style: none; padding: 0; margin: 0; }
.legend li { display: flex; align-items: center; gap: 7px; margin: 9px 0; font-size: .85rem; color: var(--muted); flex-wrap: wrap; }
.legend strong { color: var(--ink); }
.swatch { display: inline-block; width: 13px; height: 13px; border-radius: 4px; }
.content-swatch { background: #bdeee2; }.padding-swatch { background: #c8c4ff; }.border-swatch { background: #f7bd81; }.margin-swatch { background: #ffe0e6; }
.sizing-example { padding: 17px; margin: 18px 0; border-radius: 13px; background: #f8f8fd; }
.sizing-row { display: grid; grid-template-columns: 90px 1fr; gap: 9px; align-items: center; margin: 16px 0; font-size: .78rem; }
.sizing-row strong { grid-column: 2; color: var(--muted); font-size: .72rem; }
.bar { height: 18px; border-radius: 5px; background: var(--purple); }
.bar-content { width: 100%; box-shadow: 14px 0 0 #f7bd81; }
.bar-border { width: 78%; border: 3px solid #f7bd81; background: #bdeee2; }
code { padding: 2px 5px; border-radius: 5px; background: #f0efff; color: #4b43bd; font-size: .9em; }
pre { overflow-x: auto; padding: 15px; border-radius: 12px; background: #22243a; color: #f3f2ff; }
pre code { padding: 0; color: #f3f2ff; background: transparent; }
.devtools-note { display: flex; gap: 20px; padding: 27px; margin-bottom: 42px; border: 1px solid #dcd9ff; border-radius: 20px; background: #f0efff; }
.devtools-note h2 { margin-bottom: 10px; }
.devtools-note ol { margin-bottom: 0; padding-left: 21px; color: #535873; }
.devtools-note li { margin: 7px 0; }
.devtools-icon { display: grid; place-items: center; flex: 0 0 48px; height: 48px; border-radius: 15px; background: white; color: var(--purple); font-size: 1.7rem; }
footer { padding: 22px 0; background: white; border-top: 1px solid var(--line); color: var(--muted); font-size: .82rem; }
@media (max-width: 900px) { .cards-grid { grid-template-columns: 1fr 1fr; } .explain-grid { grid-template-columns: 1fr; } }
@media (max-width: 580px) { .cards-grid { grid-template-columns: 1fr; } .demo-card { width: 100%; } .controls-panel { align-items: flex-start; flex-direction: column; } .toggle-group { width: 100%; } .mode-button { flex: 1; } .devtools-note { flex-direction: column; } .explain-card { padding: 20px; } }
