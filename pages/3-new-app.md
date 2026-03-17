# Chats Mobile React Native

Ecco cosa abbiamo ottenuto finora.

<div class="grid grid-cols-4 gap-6 mt-8">
<div class="text-center p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="big-number">40</div>
<div class="subtitle">giorni di sviluppo effettivo</div>
</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="big-number">~60%</div>
<div class="subtitle">codice portato dal web</div>
</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="big-number">0</div>
<div class="subtitle">blocker tecnici incontrati</div>
</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="big-number">25.12</div>
<div class="subtitle">già compatibile Carbonio</div>
</div>
</div>

<!--
Bene, basta teoria — passiamo a quello che abbiamo costruito davvero. Quaranta giorni di sviluppo effettivo. Non quaranta giorni con un team di dieci persone, eh — quaranta giorni di lavoro. E circa il 60% del codice arriva direttamente dal web: gli store Zustand, i modelli dati, la logica di normalizzazione dei messaggi, le utility. Erano già scritti, già testati, li abbiamo portati su mobile e funzionano. Zero blocker tecnici: non ci siamo mai trovati davanti a un muro che ci ha fatto dire "questo non si può fare". E l'app è già compatibile con Carbonio 25.12. Per dare un termine di paragone: un'app nativa equivalente, scritta da zero in Swift e Kotlin, richiederebbe un team dedicato per almeno sei mesi.
-->

---

# La Chat

<div class="grid grid-cols-2 gap-8 mt-8">
<div class="p-5" style="background: rgba(97,218,251,0.08); border-radius: 8px;">

### Funzionalità core — tutto funzionante

- Conversazioni 1:1 e di gruppo
- Messaggi con allegati
- Push notification su entrambe le piattaforme
- Deep linking nelle conversazioni
- Persistenza locale veloce (MMKV)
- Credenziali gestite in modo sicuro
- Build già su TestFlight e Google Play

</div>
<div class="p-5" style="background: rgba(42,157,92,0.1); border-radius: 8px; border: 1px solid rgba(42,157,92,0.2);">

### In 40 giorni, già oltre l'app nativa

- **Pin dei messaggi**
- **Ice restart** — riconnessione automatica al cambio rete

<div class="mt-4 text-sm subtitle">
Queste feature non sono ancora presenti nell'app nativa attuale
</div>

</div>
</div>

<!--
Entriamo nel dettaglio della chat, che è la parte più matura dell'app. A sinistra vedete le funzionalità core: conversazioni 1:1 e di gruppo, messaggi con allegati, push notification su entrambe le piattaforme — FCM per Android, APNs per iOS. Deep linking, quindi se qualcuno vi manda un link a una conversazione si apre direttamente nell'app. Persistenza locale con MMKV, che è molto più veloce di AsyncStorage. Credenziali gestite in modo sicuro. E le build girano già su TestFlight e Google Play interno. Ma la cosa che mi fa più piacere è a destra: in alcuni casi siamo già oltre l'app nativa attuale. Il pin dei messaggi e l'ice restart — cioè la riconnessione automatica durante una videochiamata quando cambi rete — sono feature che l'app nativa non ha ancora. In quaranta giorni siamo andati oltre.
-->

---

# Le Videochiamate

<div class="mt-4 mb-8 subtitle">Non ancora complete, ma la parte rischiosa è fatta.</div>

<div class="grid grid-cols-4 gap-4">
<div class="text-center p-5" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="text-3xl mb-3">🔊</div>

**Audio**

Routing tra cuffie, altoparlante e vivavoce
</div>
<div class="text-center p-5" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="text-3xl mb-3">📹</div>

**Video**

Stream locale e remoto funzionanti
</div>
<div class="text-center p-5" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="text-3xl mb-3">🎧</div>

**Bluetooth**

Dispositivi rilevati e selezionabili correttamente
</div>
<div class="text-center p-5" style="background: rgba(97,218,251,0.08); border-radius: 8px;">
<div class="text-3xl mb-3">📱</div>

**CallKit iOS**

L'integrazione nativa più delicata, già funzionante
</div>
</div>

<!--
Le videochiamate sono la parte tecnicamente più delicata, e non sono ancora complete — ma qui il punto importante è un altro. La parte rischiosa è fatta. Quello che dovevamo dimostrare era che si potesse fare, e l'abbiamo dimostrato. L'audio routing funziona: cuffie, altoparlante, passaggio automatico. Il video funziona: stream locale e remoto. Il Bluetooth funziona: i dispositivi vengono rilevati e si possono selezionare. E soprattutto CallKit su iOS funziona — che è l'integrazione più delicata di tutte, quella che fa apparire la schermata di chiamata nativa del telefono quando qualcuno vi chiama. Tutto questo gira. Quello che manca è rifinitura e completamento delle feature secondarie, ed è pianificato. Non ci aspettiamo sorprese perché la parte a rischio l'abbiamo già superata.
-->