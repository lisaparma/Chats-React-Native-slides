---
layout: center
---
# React Native & Expo
---

# React Native & Expo

<br />

- **React Native**: framework open source di Meta per creare app mobile native usando JavaScript/TypeScript e React. Permette di scrivere una sola codebase per iOS e Android, con UI e performance native.

- **Expo**: piattaforma e toolchain che semplifica lo sviluppo React Native. Offre strumenti, librerie, build cloud e aggiornamenti OTA, rendendo più facile e veloce creare, testare e distribuire app mobile.

---

# Codice condiviso

```mermaid
---
config:
  treemap:
    valueFormat: '.0%'
    showValues: true
    padding: 16
    headerHeight: 36
---

treemap-beta
"Codice Carbonio Chats frontend e mobile"
    "Business Logic": 0.70:::shared
    "Web": 0.30:::web
    "Mobile":::mobileGroup
        "React Native / Expo": 0.20:::rn
        "Apple iOS": 0.05:::native
        "Android": 0.05:::native

classDef shared fill:#0e4d6e,stroke:#61dafb,stroke-width:3px,color:#ffffff,font-size:22px,font-weight:bold,rx:10,ry:10;
classDef web fill:#163d5c,stroke:#61dafb,stroke-width:2px,color:#e2e8f0,font-size:20px,rx:10,ry:10;
classDef mobileGroup fill:#0d3320,stroke:#2a9d5c,stroke-width:3px,color:#ffffff,font-size:20px,font-weight:bold,rx:10,ry:10;
classDef rn fill:#1a5c38,stroke:#2a9d5c,stroke-width:2px,color:#e2e8f0,font-size:18px,rx:10,ry:10;
classDef native fill:#133d27,stroke:#2a9d5c,stroke-width:1px,color:#94a3b8,font-size:14px,rx:10,ry:10;
```

---

# Upgrade degli SDK

React Native ed Expo semplificano sia l’upgrade degli SDK che la pubblicazione negli store:

- Upgrade SDK: Expo offre comandi e documentazione per aggiornare facilmente l’SDK, con tool che automatizzano gran parte del processo. React Native ha una community attiva e strumenti come “react-native upgrade”.
- Pubblicazione negli store: Expo fornisce build cloud, generazione automatica di pacchetti (APK/IPA) e procedure guidate per la pubblicazione su App Store e Google Play, riducendo errori e complessità.
- con Expo è possibile fare un “hot upgrade” tramite gli aggiornamenti OTA (Over The Air). E' possibile distribuire nuove versioni del codice JavaScript/TypeScript (fix, feature, UI) direttamente sui dispositivi degli utenti, senza dover ripubblicare l’app negli store

---

# Perché Ora?

<div class="grid grid-cols-2 gap-12 mt-10">
<div>

### Al tempo

<div class="p-4 mt-4" style="background: rgba(230,57,70,0.1); border-radius: 8px; border-left: 3px solid #e63946;">

- WebRTC su React Native era un incubo
- Il bridge JS/native era un collo di bottiglia
- I team erano separati, non c'era contesto condiviso

</div>
</div>
<div>

### Oggi

<div class="p-4 mt-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border-left: 3px solid #61dafb;">

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
- Performance leggermente inferiori in casi molto specifici (grafica, animazioni complesse)
</div>

<div class="p-4 mt-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border-left: 3px solid #61dafb;">

- React Native è estendibile con codice nativo
- In caso di mancato aggiornamento, feature leggermente più lente
- Solo per applicazioni molto spinte graficamente (giochi o rendering)

</div>
</div>
