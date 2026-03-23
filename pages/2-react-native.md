---
layout: center
---
# Stack tecnologico
---

# React Native & Expo

<br />

- **React Native**: 
    - framework open source di Meta 
    - usa JavaScript/TypeScript e React 
    - una sola codebase per iOS e Android
    - UI e performance native.

- **Expo**: piattaforma e toolchain che semplifica lo sviluppo React Native. 

---

# Codice condiviso frontend-mobile

```mermaid
---
config:
  treemap:
    showValues: false
    padding: 16
    headerHeight: 36
---

treemap-beta
    "Business Logic  —  70%": 0.70:::shared
    "Web  —  30%": 0.30:::web
    "Mobile":::mobileGroup
        "React Native / Expo  —  20%": 0.20:::rn
        "Apple iOS  —  10%": 0.10:::native
        "Android  —  10%": 0.10:::native

classDef shared fill:#0e4d6e,stroke:#61dafb,stroke-width:3px,color:#ffffff,font-size:22px,font-weight:bold,rx:10,ry:10;
classDef web fill:#163d5c,stroke:#61dafb,stroke-width:2px,color:#e2e8f0,font-size:20px,rx:10,ry:10;
classDef mobileGroup fill:#0d3320,stroke:#2a9d5c,stroke-width:3px,color:#ffffff,font-size:20px,font-weight:bold,rx:10,ry:10;
classDef rn fill:#1a5c38,stroke:#2a9d5c,stroke-width:2px,color:#e2e8f0,font-size:18px,rx:10,ry:10;
classDef native fill:#133d27,stroke:#2a9d5c,stroke-width:1px,color:#94a3b8,font-size:14px,rx:10,ry:10;
```

---

# Gestione delle applicazioni negli store 

<br />

- Processo di rilascio più snello e automatizzato
- Pubblicazione sugli store più semplice
- Possibilità di aggiornamenti OTA (Over The Air), bypassando in alcuni casi l'approvazione di Apple/Google
- Una sola pipeline di rilascio per entrambe le piattaforme
---

# Perché ora?

<div class="grid grid-cols-2 gap-12 mt-10" style="grid-auto-rows: 1fr;">
<div style="display: flex; flex-direction: column;">

### 2019

<div class="p-4 mt-4" style="background: rgba(230,57,70,0.1); border-radius: 8px; border-left: 3px solid #e63946; flex: 1;">

- La gestione delle videochiamate su React Native era più complessa
- Il bridge JS/native era un collo di bottiglia

</div>
</div>
<div style="display: flex; flex-direction: column;">

### Oggi

<div class="p-4 mt-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border-left: 3px solid #61dafb; flex: 1;">

- **New Architecture** stabile, bridge rimosso
- **Expo EAS** affidabile in produzione
- La nostra logica web è matura e pronta da portare

</div>
</div>
</div>

---

# Rischi

<div class="grid  grid-cols-2 gap-12 mt-10">
<div class="p-4 mt-4" style="background: rgba(230,57,70,0.1); border-radius: 8px; border-left: 3px solid #e63946;">

- Alcune API native non hanno wrapper pronti, servono moduli custom
- La New Architecture è stabile ma giovane
</div>

<div class="p-4 mt-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border-left: 3px solid #61dafb;">

- React Native è estendibile con codice nativo
- In caso di mancato aggiornamento, feature leggermente più lente

</div>
</div>
