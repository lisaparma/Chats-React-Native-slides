---
theme: default
title: Chats Mobile – React Native + Expo
colorSchema: dark
fonts:
  sans: DM Sans
  mono: DM Mono
---
<style>
@import url('https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;0,9..40,700&family=DM+Mono:wght@400;500&display=swap');

:root {
  --slidev-theme-primary: #61dafb;
}

/* — Base — */
.slidev-layout {
  background: #1a1a2e;
  color: #e2e8f0;
  font-family: 'DM Sans', sans-serif;
}

/* — Tipografia — */
.slidev-layout h1 {
  color: #61dafb;
  font-weight: 700;
  letter-spacing: -0.02em;
  border-bottom: none !important;
}

.slidev-layout h2 {
  color: #61dafb;
  font-weight: 600;
  opacity: 0.9;
}

.slidev-layout h3 {
  color: #94a3b8;
  font-weight: 400;
  letter-spacing: 0.02em;
}

.slidev-layout strong {
  color: #f1f5f9;
  font-weight: 600;
}

.slidev-layout a {
  color: #61dafb;
  text-decoration: none;
  border-bottom: 1px solid rgba(97, 218, 251, 0.3);
}

/* — Liste — */
.slidev-layout li {
  line-height: 1.8;
}

.slidev-layout li::marker {
  color: #61dafb;
}

/* — Code — */
.slidev-layout code {
  background: rgba(97, 218, 251, 0.1);
  color: #61dafb;
  border-radius: 4px;
  padding: 2px 6px;
  font-family: 'DM Mono', monospace;
  font-size: 0.9em;
}

/* — Tabelle — */
.slidev-layout table {
  width: 100%;
  border-collapse: separate;
  border-spacing: 0;
}

.slidev-layout th {
  background: rgba(97, 218, 251, 0.15);
  color: #61dafb;
  font-weight: 600;
  text-align: left;
  padding: 12px 16px;
  border-bottom: 2px solid rgba(97, 218, 251, 0.3);
}

.slidev-layout td {
  padding: 10px 16px;
  border-bottom: 1px solid rgba(226, 232, 240, 0.1);
}

.slidev-layout tr:hover td {
  background: rgba(97, 218, 251, 0.05);
}

/* — Slide di sezione (cover) — */
.slidev-layout.section-title {
  background: linear-gradient(135deg, #1a1a2e 0%, #16213e 100%);
  display: flex;
  align-items: center;
  justify-content: center;
}

/* — Badge sezione (in alto a destra) — */
.slidev-layout.section-map::before,
.slidev-layout.section-react::before,
.slidev-layout.section-app::before,
.slidev-layout.section-next::before {
  position: fixed;
  bottom: 12px;
  padding: 3px 10px;
  border-radius: 20px;
  font-size: 0.72em;
  font-weight: 600;
  font-family: 'DM Sans', sans-serif;
  letter-spacing: 0.03em;
  z-index: 100;
}

.slidev-layout.section-map::before {
  content: 'Team';
  left: 2%;
  background: rgba(230,57,70,0.15);
  color: #e63946;
  border: 1px solid rgba(230,57,70,0.3);
}

.slidev-layout.section-react::before {
  content: 'React Native';
  left: 27%;
  background: rgba(97,218,251,0.15);
  color: #61dafb;
  border: 1px solid rgba(97,218,251,0.3);
}

.slidev-layout.section-app::before {
  content: "L'App";
  left: 52%;
  background: rgba(42,157,92,0.15);
  color: #2a9d5c;
  border: 1px solid rgba(42,157,92,0.3);
}

.slidev-layout.section-next::before {
  content: "What's Next";
  left: 77%;
  background: rgba(244,194,13,0.15);
  color: #f4c20d;
  border: 1px solid rgba(244,194,13,0.3);
}

/* — Progress bar — */
.slidev-layout.section-map::after,
.slidev-layout.section-react::after,
.slidev-layout.section-app::after,
.slidev-layout.section-next::after {
  content: '';
  position: fixed;
  bottom: 0;
  left: 0;
  width: 100%;
  height: 4px;
  pointer-events: none;
  z-index: 100;
  background: linear-gradient(to right,
    rgba(230,57,70,0.2) 0% 25%,
    rgba(97,218,251,0.2) 25% 50%,
    rgba(42,157,92,0.2) 50% 75%,
    rgba(244,194,13,0.2) 75% 100%
  );
}

.slidev-layout.section-map::after {
  background: linear-gradient(to right,
    #e63946 0% 25%,
    rgba(97,218,251,0.2) 25% 50%,
    rgba(42,157,92,0.2) 50% 75%,
    rgba(244,194,13,0.2) 75% 100%
  );
}
.slidev-layout.section-react::after {
  background: linear-gradient(to right,
    rgba(230,57,70,0.2) 0% 25%,
    #61dafb 25% 50%,
    rgba(42,157,92,0.2) 50% 75%,
    rgba(244,194,13,0.2) 75% 100%
  );
}
.slidev-layout.section-app::after {
  background: linear-gradient(to right,
    rgba(230,57,70,0.2) 0% 25%,
    rgba(97,218,251,0.2) 25% 50%,
    #2a9d5c 50% 75%,
    rgba(244,194,13,0.2) 75% 100%
  );
}
.slidev-layout.section-next::after {
  background: linear-gradient(to right,
    rgba(230,57,70,0.2) 0% 25%,
    rgba(97,218,251,0.2) 25% 50%,
    rgba(42,157,92,0.2) 50% 75%,
    #f4c20d 75% 100%
  );
}

/* — Utility per evidenziare numeri grandi — */
.big-number {
  font-size: 3em;
  font-weight: 700;
  color: #61dafb;
  line-height: 1.2;
}

.subtitle {
  color: #94a3b8;
  font-size: 0.95em;
}
</style>

<div class="flex items-center gap-16 h-full">
<img src="/icon-blu.png" class="rounded-xl shrink-0" style="max-height: 250px; object-fit: cover;" />
<div>

# Chats Mobile
## in React Native

</div>
</div>

---
class: section-map
src: ./pages/1-vertical-team.md
---

---
class: section-react
src: ./pages/2-react-native.md
---

---
class: section-app
src: ./pages/3-new-app.md
---

---
class: section-next
src: ./pages/4-whats-next.md
---