# Riunione 24 Maggio 2021 - Disamina Report VoiceMath

## DLM :
per ora contempla solo discorsi non interrotti.

**Alessandro Mazzei**: 
1. andrebbe ampliato il DLM, includendo più diciture matematiche.
2. questione del parlato spontaneo. Non è fattibile annullarlo completamente.


## BASELINE:
**Adriano Sofia**:
Potremmo sottoporre gli stessi video a google per comparare la qualità dei risultati.
**Francesco Tarasconi**: è una cosa di cui abbiamo discusso, lo faremo tempo permettendo.

## AUDIO
**Alessandro Mazzei**:  è necessario dare una quantificazione dei problemi.
         L'approccio usato finora è solo qualitativo:
         Qual è il benchmark? Chi ci fornisce dei parametri per dichiarare quanto rumore è tollerabile e quanto non tollerabile?
        
**Cristian Bernareggi**: le immagini sottoposte ad OCR: come le sincronizzi con il video?
         **Francesco Tarasconi**: il design di questa parte verrà fatto a Giugno/Luglio.

**Davide Maietta**: È possibile un approccio in cui un umano corregga i punti più critici (esempio: formule complesse)?
Le informazioni aggiunte dal correttore umano potrebbero confluire nel DLM, arricchendo il DLM del sistema. 
(addestramento supervisionato)
**Francesco Tarasconi** Il fine tuning è possibile (ma sconsigliato) via DLM (di competenza esclusiva di un linguista), via 
Dizionario(dove comunque si sconsiglia di allungare troppo il dizionario) e via iperparametri(di setup del sistema).
Non esiste, invece, possibilità di fine-tuning con integrazioni sul training set.

**Alessandro Mazzei**: 
## QUANTIFICARE GLI EFFETTI
Le conclusioni del report sono sempre troppo qualitative.
Vorremmo delle misurazioni per validare un ragionamento:
1. Quanto incide una ripetizione?
2. Quanto incide una frase interrotta?
3. Quanto incide l'audio in sé?
4. Quanto incide il microfono/la distanza dal parlante/il rimbombo?

Francesco Tarasconi: impostare un'analisi quantitativa che sia stata sottoposta  a controllo a campione.
Marcare le porzioni di discorso come "verbale" o "matematico".
Verranno fatti dei cluster dell'audio:
Cluster "audio buono"/"audio con rumore di fondo"/cluster intermedi: le metriche verranno applicate su tali cluster di trascrizioni.
Dovrà anche essere considerato (audio buono, trascrizione golden buona)


## MathPix: non è addestrabile 
**Francesco Tarasconi**: conferma, non è addestrabile; preprocessing e postprocessing possono aiutare a dare correzioni. 
                         Quando MathPix confonde un carattere per un altro, si impone una correzione. 
                         Utente esperto può imporre correzione sistematica, ma potrebbe introdurre errori sistematici.
Per le formule:
-- vorremmo avere output **Francesco Tarasconi**: promette di fornirci output.
-- confronto con altri sistemi? (equatio, infty)


