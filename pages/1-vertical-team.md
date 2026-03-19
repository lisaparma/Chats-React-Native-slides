# Da Team Orizzontali a Verticali

Due anni fa abbiamo riorganizzato i team per prodotto, non più per competenza.

<div class="mt-8">

- 🏗️ **End-to-end** — ogni team possiede il suo dominio dall'inizio alla fine
- 🚫 **Zero handoff** — una feature non passa più per 2-3 team diversi
- 🎯 **Ownership** — chi firma il prodotto sa sempre cosa succede e perché
- ⚡ **Velocità** — dal ticket al deploy senza code tra team
- 🔍 **Qualità** — chi costruisce è chi mantiene, gli standard restano alti

</div>

---

# I Risultati

<div class="grid grid-cols-2 gap-6 mt-8">
<div class="p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">

**Meno handoff**

Meno riunioni di allineamento, meno ticket che rimbalzano

</div>
<div class="p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">

**Dominio condiviso**

Chi entra nel team capisce subito il perimetro

</div>
<div class="p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">

**Bug fix rapidi**

Chi fixa il bug è chi ha scritto il codice

</div>
<div class="p-4" style="background: rgba(97,218,251,0.08); border-radius: 8px;">

**Roadmap chiara**

Nessuna zona grigia su chi fa cosa

</div>
</div>

---

# Il Nostro Team Oggi

<div class="flex flex-col items-center justify-center mt-6">
    <ul style="list-style: none; padding: 0; margin: 0; text-align: center;">
        <li>- fontrendisti</li>
        <li>- backendisti</li>
        <li>- ux designer</li>
    </ul>
</div>

<div class="mt-10 text-xl leading-relaxed">

Gestiamo **chat, videochiamate e files** di Carbonio, end-to-end.

Web e backend, dalla progettazione alla produzione. Quando arriva un bug o una feature, non serve coordinarsi con nessun altro.

<div class="mt-8 p-4 text-center" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">
Un unico team · Zero dipendenze esterne · Dalla segnalazione al fix
</div>
</div>
---

# Ulteriore verticalizzazione

<div class="mt-8">

Aggiungere il **client mobile**.

<div class="grid grid-cols-3 gap-6 mt-8">
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Stesso Team**

Chi sviluppa il mobile ora conosce il backend.

</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Features "quasi" unica**

Ora le feature sviluppate dal front end sono riutilizzabili l'80% anche nel mobile

</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Bug fix veloce x2**

Chi risolve il bug conosce il contesto e la stessa correzione può essere condivisa tra frontend e mobile

</div>
</div>
</div>

<!--
Però c'è un pezzo che manca, ed è il punto cruciale di tutta questa presentazione. Il client mobile — l'app che gli utenti usano su telefono — è ancora gestito da un team diverso dal nostro. Pensateci: è esattamente la situazione che la verticalizzazione doveva eliminare. Ogni nuova feature della chat va spiegata due volte, a due team diversi. Ogni bug mobile coinvolge persone che non hanno il contesto del backend. I tempi si allungano, la qualità ne risente. Finché il mobile resta fuori dal nostro perimetro, l'investimento nella verticalizzazione è incompleto. Manca l'ultimo miglio.
-->

---

# Come Chiudiamo il Cerchio

<div class="mt-8">

React Native porta il mobile **dentro il team Chats**.

<div class="grid grid-cols-3 gap-6 mt-10">
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Stesso stack**

TypeScript, React, Zustand — niente di nuovo da imparare

</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Stessa logica**

Il codice di business è già scritto e già testato

</div>
<div class="text-center p-4" style="background: rgba(97,218,251,0.1); border-radius: 8px; border: 1px solid rgba(97,218,251,0.2);">

**Stessa persona**

Chi lavora sul web può lavorare sul mobile

</div>
</div>

<div class="mt-8 text-center text-lg" style="color: #61dafb;">
Un team → tutti i client: web, iOS, Android
</div>
</div>

<!--
E qui entra in gioco React Native. È la tecnologia che ci permette di chiudere il cerchio. Perché? Perché è basata su React e TypeScript — esattamente lo stack che usiamo già tutti i giorni per il web. Non dobbiamo imparare un linguaggio nuovo, non dobbiamo assumere persone nuove. La logica di business — gli store Zustand, i modelli dati, le regole — è già scritta e già testata sul web. La portiamo su mobile così com'è. La stessa persona che lavora su una feature web può lavorare sulla stessa feature mobile. Un team, tutti i client: web, iOS, Android. Questo è il completamento naturale della verticalizzazione.
-->
