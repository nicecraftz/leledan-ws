<template>
  <div class="min-h-screen bg-background text-text">
    <NavBar class="sticky top-0 z-10 bg-background" />
    <div class="flex items-center justify-center py-6 md:py-10 px-1 md:px-2 mx-5">
      <div class="w-full max-w-5xl mx-auto">
        <h1 class="text-2xl md:text-3xl font-extrabold text-primary mb-8 text-center">Termini di Servizio (TOS)</h1>
        <div class="grid grid-cols-1 md:grid-cols-2 gap-4 md:gap-5">
          <!-- 1 - IMPEGNO -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">1. Impegno</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>Tutte le richieste verranno esaminate e devono essere conformi a questi Termini di Servizio.</li>
              <li>I lavori vengono selezionati manualmente, l'artista sceglie i progetti su cui lavorare. Alcune richieste possono essere rifiutate senza giustificazione.</li>
              <li>Dopo l'accettazione, il cliente riceverà una conferma d'ordine e potrà seguire i progressi tramite messaggio diretto.</li>
              <li>Il cliente deve fornire tutte le informazioni e i riferimenti necessari prima dell’inizio del lavoro (immagini, descrizione, stile desiderato e altro) preferibilmente in un unico file/cartella (PDF, Google Docs, ecc.).</li>
              <li>Il cliente concede all’artista il diritto di usare i riferimenti solo per l'opera richiesta e garantisce di detenere i diritti su tutti i materiali forniti.</li>
              <li>L’artista si impegna a lavorare in buona fede e con dedizione, garantendo originalità e realizzando l'opera al meglio delle proprie conoscenze, anche con materiali o risorse ad uso commerciale o libero.</li>
              <li>L’artista può rifiutare richieste con contenuti offensivi, illegali o che non si adattano allo stile o tema.</li>
            </ul>
          </div>
          <!-- 2 - SCADENZE E PROCESSO -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">2. Scadenze e processo</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>Il tempo di consegna standard è tra i 2 e i 7 giorni lavorativi, in base alla complessità e alla lista d’attesa.</li>
              <li>Il cliente riceverà una bozza iniziale per approvazione prima del pagamento definitivo.</li>
              <li>L’artista aggiorna volontariamente sullo stato, ma il cliente può chiedere aggiornamenti durante il processo (senza inviare messaggi quotidiani).</li>
              <li>La consegna finale avviene su Discord, Telegram o email, in formato .schem. Il cliente riceve solo la versione finale esportata.</li>
              <li>Eventuali modifiche sulle scadenze saranno comunicate in anticipo.</li>
            </ul>
          </div>
          <!-- 3 - RESTRIZIONI SUI CONTENUTI -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">3. Restrizioni sui contenuti</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>L’artista non accetta lavori che coinvolgono: contenuti sessualmente espliciti, gore estremo, temi offensivi o discriminatori, uso improprio di immagini di persone reali, imitazione diretta di stili o opere di altri artisti.</li>
            </ul>
          </div>
          <!-- 4 - REVISIONI E MODIFICHE -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">4. Revisioni e modifiche</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>Fino a 3 revisioni gratuite durante la fase di bozza.</li>
              <li>Dopo l’approvazione finale, solo piccole correzioni (es. colori o dettagli minori) saranno gratuite.</li>
              <li>Modifiche importanti o eccessive possono comportare costi aggiuntivi, comunicati prima dell’esecuzione.</li>
              <li>Il cliente non può alterare, modificare o ridisegnare l’opera finale senza il permesso dell’artista.</li>
            </ul>
          </div>
          <!-- 5 - COMUNICAZIONE -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">5. Comunicazione</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>La comunicazione avviene solo tramite Discord, Telegram o email.</li>
              <li>Il tempo di risposta dell’artista può arrivare a 3 giorni lavorativi.</li>
              <li>Se il cliente non risponde per 7 giorni senza preavviso, l’ordine può essere considerato abbandonato e terminato senza rimborso.</li>
            </ul>
          </div>
          <!-- 6 - DIRITTI D'USO -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">6. Diritti d'uso</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>L’artista conserva diritti d’autore e di pubblicazione sull’opera e può mostrarla in portfolio/social, tranne quando il cliente chiede riservatezza.</li>
              <li>Il cliente ottiene il diritto d’uso personale e a scopo di lucro.</li>
              <li>L’esclusività totale o trasferimento di diritti deve essere concordato in anticipo e per iscritto.</li>
              <li class="mt-2"><span class="font-bold text-warning">⚠️</span> L’acquisto non concede i diritti sul file sorgente o di modifica.<br>
                Per le Build: file in formato (.schematic, .schem).<br>
                Per le Skin: file in formato (PNG).</li>
            </ul>
          </div>
          <!-- 7 - PAGAMENTO -->
          <div class="bg-primary/10 rounded-xl shadow-primary shadow-md border-2 border-primary p-5 mb-2 animate-fade-in">
            <h2 class="text-xl font-bold text-primary mb-3">7. Pagamento</h2>
            <ul class="list-disc pl-5 space-y-1">
              <li>Pagamento tramite PayPal o bonifico bancario.</li>
              <li>Il pagamento va effettuato solo dopo l’approvazione della bozza.</li>
              <li>Ordini non pagati entro 48 ore dall’invio della fattura possono essere annullati.</li>
            </ul>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>