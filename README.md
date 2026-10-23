# Unwrap per Windows

**Apri con un doppio clic i file firmati digitalmente `.p7m` e `.m7m` e vedi subito il documento contenuto** — PDF, fattura elettronica impaginata, XML, JSON, testo o immagine — senza dover installare programmi di firma. La verifica della firma c'è, ma solo quando la chiedi.

Questa è la versione per **Windows 11** di Unwrap, l'app che esiste anche per macOS. Gratuita, senza pubblicità, senza statistiche.

> ## ⚠️ Versione beta
> Unwrap per Windows è in **beta**: le funzioni principali ci sono, ma l'app è stata provata su poche macchine e mancano ancora cose (schede, stampa, estrazione in blocco, trascinamento fuori dalla finestra…). Può avere difetti. Se trovi un problema, apri una segnalazione nella sezione **Issues** di questa pagina: dì cosa stavi facendo e, se puoi, la versione che trovi in *Impostazioni ▸ Informazioni*. **Non allegare documenti veri.**

## Scaricare e installare

1. Vai su **[Releases](../../releases/latest)** e scarica `Unwrap-…-win-x64-Setup.exe`.
2. Avvialo e segui la procedura (serve la conferma dell'amministratore). Dopo l'installazione il doppio clic su un `.p7m` o `.m7m` apre Unwrap.

Requisiti: **Windows 11**, 64 bit (sui PC con processore ARM dovrebbe girare in emulazione, ma non è stato ancora provato).

**L'installer non è firmato** con un certificato a pagamento (per ora). Alla prima apertura Windows può mostrare *«Windows ha protetto il PC»*: scegli **Ulteriori informazioni ▸ Esegui comunque**. Per controllare di aver scaricato il file giusto, nelle note di ogni release trovi la sua impronta SHA-256.

## Cosa fa

- Apre `.p7m` (DER, Base64, PEM), buste annidate, firme *detached*, `.m7m` e allegati di PEC `.eml`; riconosce il tipo di documento dai byte, non dall'estensione.
- Mostra PDF, fatture elettroniche impaginate su fogli A4, XML e JSON rientrati e colorati, testo con ricerca, immagini.
- Pannello laterale con i dati del file, del contenuto e dei firmatari.
- **Verifica firma** su richiesta: integrità, catena dei certificati, revoca, marche temporali, con le liste di fiducia eIDAS italiana ed europea.
- Italiano e inglese, tema chiaro e scuro.

## Privacy

Aprire e leggere i file è **100% locale**: il contenuto resta in memoria e non viene mai inviato a nessuno. L'app fa richieste di rete **solo** in questi casi, e se non usi queste funzioni non ne fa nessuna:

1. scaricare **una volta** il foglio di stile della fattura, dopo il tuo permesso;
2. **Verifica firma**, solo quando premi il pulsante (si contattano i servizi di revoca dei certificati e le liste di fiducia; il documento non viene mai inviato);
3. **cercare aggiornamenti**: legge un piccolo file di questa pagina, con la frequenza che scegli nelle Impostazioni (di serie una volta al mese, oppure «Mai»). Non invia né documenti né informazioni sul tuo computer (come per qualunque sito, GitHub vede il tuo indirizzo IP), e scarica e installa solo se confermi. L'aggiornamento è firmato e l'app rifiuta quello con firma non valida;
4. aprire il browser su un link (donazione, assistenza), solo se ci clicchi.

Nessun tracciamento, nessuna pubblicità, nessuna libreria di terzi che raccoglie dati.

## Limite importante

Unwrap **non è un validatore con pieno valore legale**: non copre tutti gli aspetti di una validazione a lungo termine. La verifica della firma è un aiuto per capire cosa c'è in un file, non un parere legale.

## Il codice sorgente

Questa pagina serve solo a distribuire l'app: **contiene gli installer e gli aggiornamenti, non il codice**. Il repository di sviluppo (`unwrap-win`) è **privato**. Tutti i diritti riservati © Francesco Tarini; non c'è una licenza open source.
