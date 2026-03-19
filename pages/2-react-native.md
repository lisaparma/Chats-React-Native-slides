# Perché React Native?

## Cos'è

<br />

- **React Native**: framework open source di Meta per creare app mobile native usando JavaScript/TypeScript e React. Permette di scrivere una sola codebase per iOS e Android, con UI e performance native.

- **Expo**: piattaforma e toolchain che semplifica lo sviluppo React Native. Offre strumenti, librerie, build cloud e aggiornamenti OTA, rendendo più facile e veloce creare, testare e distribuire app mobile.

<!--
Voglio essere chiara su un punto: React Native non è "il meno peggio". Per il nostro contesto specifico, è la scelta migliore. Stesso linguaggio — TypeScript e React — significa che chiunque nel team può contribuire al mobile dal giorno uno, senza formazione aggiuntiva. Il codice condiviso non è un'aspirazione: è realtà. Gli store Zustand, la logica di normalizzazione dei messaggi, le utility — le abbiamo già portate e funzionano. React Native compila in componenti nativi veri, non è una WebView mascherata. E se mai dovessimo fare qualcosa che React Native non offre di suo — per esempio un'integrazione molto specifica con il sistema operativo — possiamo sempre scrivere un modulo nativo in Swift o Kotlin. Non siamo mai bloccati.
-->

---

# Perché react Native? - Stesso linguaggio

<div class="flex flex-col items-start w-full">

<div class="p-8 w-full max-w-3xl" style="background: rgba(97,218,251,0.08); border-radius: 12px;">
<div class="text-lg">
React Native utilizza:
</div>

<div class="text-lg">
<div class="flex flex-col items-start">
    <ul class="list-disc text-lg my-6">
        <li><strong>TypeScript</strong></li>
        <li><strong>React</strong></li>
        <li><strong>Zustand</strong></li>
    </ul>
</div>
<div class="text-lg mt-8">
    Gli stessi strumenti che già usiamo per il web. Questo permette a tutto il team di contribuire allo sviluppo mobile fin dal primo giorno, senza la necessità di apprendere nuove tecnologie o affrontare curve di apprendimento aggiuntive.
</div>
</div>
</div>

</div>

---

# Perché react Native? - Codice condiviso

```mermaid
flowchart LR
    subgraph Web
        direction TB
        A[Frontend Web<br/>React + TypeScript]
    end
    subgraph Mobile
        direction TB
        B[App Mobile<br/>React Native + TypeScript]
        B1[iOS]
        B2[Android]
        B --> B1
        B --> B2
    end
    subgraph Shared["Business Logic<br/>Zustand + TypeScript"]
        direction TB
        S[Store, Models,<br/>API, WebSocket]
    end

    S -- "riuso" --> A
    S -- "riuso" --> B

    style Web fill:#1565c0,stroke:#2196f3,stroke-width:2px,color:#fff
    style Mobile fill:#1565c0,stroke:#2196f3,stroke-width:2px,color:#fff
    style Shared fill:#1976d2,stroke:#2196f3,stroke-width:2px,color:#fff
    style S fill:#29b6f6,stroke:#2196f3,stroke-width:2px,color:#212121
    style A fill:#29b6f6,stroke:#2196f3,stroke-width:2px,color:#212121
    style B fill:#29b6f6,stroke:#2196f3,stroke-width:2px,color:#212121
    style B1 fill:#1565c0,stroke:#2196f3,stroke-width:1px,color:#fff
    style B2 fill:#1565c0,stroke:#2196f3,stroke-width:1px,color:#fff
```

<div class="mt-6 text-center text-lg" style="color: #fff; background: #1565c0; border-radius: 8px; padding: 16px;">
La business logic è definita nello store Zustand<br>e include anche chiamate API e gestione WebSocket.<br>
Tutto questo può essere riutilizzato sia dalla Web UI che da React Native.
</div>

---

# Perché react Native? - Compilato nativo

- Scrivi il codice in JavaScript/TypeScript usando React.
- Il codice viene eseguito da un motore JavaScript (Hermes/JSC) all’interno dell’app.
- I componenti React Native non sono webview: sono mappati su veri componenti nativi (UIView su iOS, View su Android).
- La comunicazione tra JS e codice nativo avviene tramite un “bridge” (nelle nuove versioni, tramite la New Architecture e JSI).
- Il risultato: UI e performance native, con logica condivisa tra piattaforme.

---

# Perché react Native? - Estensibile

- Se serve una funzionalità non disponibile, puoi scrivere moduli nativi in Swift (iOS) o Kotlin/Java (Android)
- React Native espone API per integrare facilmente codice nativo
- Expo supporta moduli nativi tramite Expo Modules o “eject”
- Così puoi accedere a tutte le feature hardware e OS, senza limiti

---

# Perché react Native? - Upgrade degli SDK

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

<!--
Un'altra domanda legittima: "Se React Native è così bello, perché non l'avete fatto prima?" La risposta è semplice: prima non era pronto. Quando abbiamo iniziato la verticalizzazione due anni fa, React Native aveva ancora il vecchio bridge JavaScript che era un collo di bottiglia per le performance. WebRTC su React Native era un incubo. Expo non supportava ancora build in produzione in modo affidabile. Oggi è tutto cambiato. La New Architecture è stabile e rimuove il bridge. Expo con EAS ci dà build cloud, deploy automatizzati, aggiornamenti OTA. E nel frattempo la nostra logica web si è consolidata: gli store, i modelli, le API — tutto maturo e pronto per essere portato su mobile. Il timing è perfetto: la tecnologia è pronta e noi siamo pronti.
-->

---

# Contro e Rischi

<div class="grid mt-8">
<div class="p-5" style="background: rgba(230,57,70,0.1); border-radius: 8px; border-left: 3px solid #e63946;">

- Alcune API native non hanno wrapper pronti, servono moduli custom
- Il debug su device fisico è più complesso del browser
- La New Architecture è stabile ma giovane, la community sta migrando
- Performance leggermente inferiori in casi molto specifici (grafica, animazioni complesse)
</div>
</div>

<!--
Questa è la slide dell'onestà, e ci tengo. Non voglio fare solo propaganda. I pro li abbiamo visti e sono solidi: stack condiviso, riutilizzo reale del codice, performance native, aggiornamenti OTA. Ma ci sono anche dei contro e dei rischi che stiamo gestendo. Alcune API native — per esempio la gestione avanzata dell'audio Bluetooth — non hanno wrapper React Native pronti e dobbiamo scrivere moduli custom. Il debug su un dispositivo fisico è oggettivamente più complesso che aprire i DevTools del browser: ci sono più variabili, più cose che possono andare storte. E la New Architecture di React Native è stabile, sì, ma è giovane — la community la sta ancora adottando e non tutti i pacchetti di terze parti sono aggiornati. Detto questo, il bilancio per il nostro caso d'uso è nettamente positivo. I rischi sono gestibili e li stiamo gestendo.
-->
