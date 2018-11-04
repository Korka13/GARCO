---
title: "Scaricare il Tema Del Sito Su Hugo"
date: 2018-09-20T21:14:24+03:00
lastmod:
draft: false
image: "img/barbera.PNG"
categories: ["WEB"]
keywords: []
description: "In questa guida viene spiegato come scaricare e installare uno dei tanti temi su Hugo static site generator usando git, offerto il tema di questo sito e spiegati i comandi che Hugo da a disposizione per abilitare il localserver e pubblicare la versione finale del sito web"
weight: -29
---
*[Vai all'Indice completo della guida su come creare un sito come questo](/post/come-costruire-questo-blog-a-costo-zero-indice/)*

Hugo è un'ottima scelta per creare un blog in quanto offre una larga scelta di temi da cui partire, dal più semplice e basilare fino al più complesso.
Cominciate a dare un'occhiata alla <a href="https://themes.gohugo.io/" target="&#95;blank">pagina di esposizione dei temi</a> se non l'avete già fatto.
Il tema che ho scelto io è <a href="https://themes.gohugo.io/hugo-nederburg-theme/" target="&#95;blank">NEDERBURG</a>, al quale ho apportato qualche modifica. Nei prossimi articoli spiegherò nel dettaglio come ho implementato la maggior parte delle cose, quindi potete scegliere qualunque tema e applicare poi ad esso le modifiche che vi interessano.
Se volete dare un'occhiata al risultato del mio sito da parte Hugo ho creato un <a href="https://github.com/Korka13/BARBERA-theme" target="&#95;blank">repository su GitHub</a> che potete scaricare e installare sul vostro sito come un tema; io nella guida userò questo link come esempio, ma voi sostituitelo con il link del repository del tema che avete scelto.
*Piccola parentesi sulle modifiche che ho fatto sul tema, se non vi interessa skippate direttamente all'installazione!:*

- La cosa più significativa, e che potrebbe far scegliere di non usare il tema è che ho rimosso i tags e lasciato solo le categorie. Per il mio blog trovavo i tags confusionari e inutili, quindi li ho rimossi, non vengono visualizzati più nell'apposito spazio nelle pagine e tramite indicazione nel config.toml non vengono neanche create le pagine html sul sito.
- Ho tradotto (credo) tutto in italiano
- Ho modificato leggermente i colori, da una tonalità di marrone a una tonalità di grigio
- Ho rimosso la trasformazione del testo tutta in maiuscolo, per avere le parti scritte tutte in maiuscolo vanno inserite già maiuscole
- Ho rimosso il tasto Home, in quanto basta cliccare sul titolo del sito per tornare alla pagina iniziale
- Nella navbar invece di avere: **// Categoria 1 Categoria uno** abbiamo: **/ Categoria 1 Categoria 2 /**
- Nel page title (quello che si vede scritto nella tab del browser) metadata ho fatto in modo che venga visualizzato solo il **Titolo** prima era **Titolo - Slogan**
- Nella homepage nella visualizzazione dei post ho eliminato l'autore e la data e lasciato solo la categoria. Data e autore si vedono all'interno del post
- Ho aggiunto la data di ultimo aggiornamento all'interno del post. Se nel front matter è presente una data di aggiornamento viene visualizzata la data di creazione
- Nel default post archetype ho aggiunto il weight: viene calcolato automaticamente assegnando un numero più alto di dieci in dieci in negativo all'ultimo post. Quindi di default, l'ultimo post sarà più in alto. Ho fatto questo per dare la possibilità di spostare un post più in basso anche se è più nuovo. Per esempio a me è utile per questa guida, voglio che venga visualizzata in sequenza e non al contrario. Se rimuovete il weight i post vengono ordinati automaticamente in base alla data.
- Ho aggiunto la pagina della privacy
- Ho aggiunto il popup di informativa dei cookies
- Ho aggiunto la possibilità di integrare Google Adsense, basta inserire il publisher id nel config file
- Ho cambiato la favicon e il nome! Perché **BARBERA**? non ci ho perso molto tempo, cercavo una favicon gratis da implementare, quando ho visto la bottiglia di vino mi è piaciuta quindi l'ho scaricata. Poi non sapevo come chiamare il tema, allora ho cercato che cosa vuol dire **NEDERBURG**, ed è un vino! a questo punto non poteva essere altro che BARBERA.

**Ok, proseguiamo con l'installazione del tema:**

Su ogni tema ci sono le istruzioni di come installarlo, ma ognuno dice un po' i comandi che gli aggradano di più, quindi facciamola semplice:
Dalla linea di comando dovete recarvi nella cartella *themes* e poi dare il comando a git di scaricare dal repository di Github. Quindi:

* Aprite il terminal dal + in basso e dovrebbe aprirsi già nella cartella del sito, poi:
```cd themes```
e poi:
```git clone https://github.com/Korka13/BARBERA-theme.git```

Come anticipavo ho usato come esempio il link di BARBERA-theme, ma potete semplicemente sostituire il link con quello del repository che avete scelto.
Scelto il tema cliccate su download e verrete ridirezionati sulla pagina di github che ospita il tema. Il link può essere copiato dal tasto clone or download (che poi è anche il link su cui già siete ma con aggiunto .git, non ancora capito a cosa serve perché anche senza .git sembra funzionare). In alternativa potete anche scaricare il file zip e decomprimerlo nella cartella themes, ma così secondo me è più comodo.

Tutti i temi hanno al loro interno un examplesite folder, e un config.toml. Spostate i contenuti della cartella examplesite nelle corrispettive cartelle del vostro sito e sostituite il config.toml del vostro sito con quello scaricato del tema.

Attenzione che nel config.toml, dove c'è scritto **theme** accanto riporti l'esatto nome della cartella del tema

Adesso il tema è installato. Per vedere il sito live nel browser:
Nel terminal fate attenzione ad essere nella cartella principale del sito. Se siete ancora nella cartella themes:
```cd..```
Per tornare indietro e poi:
```hugo server```
Questo abilita un local server di hugo che trasforma live i contenuti del sito in html vero e proprio e vi da la possibilità di vedere il sito aggiornarsi in locale mentre ci lavorate, prima di costruire il sito per caricarlo online.
Questa live preview la potete vedere andando su:
<a href="http://localhost:1313/" target="_blank">localhost:1313</a>
La finestra del terminal non sarà utilizzabile mentre manda il sito in preview, ma cliccando di nuovo sul + ne potete aprire una seconda.
Per stoppare il terminal dalla preview premete contemporaneamente Ctrl + C
Per gli impazienti scrivo già qui come creare la cartella con i file html da caricare online per non farvi impazzire a cercare il comando negli articoli seguenti. Il comando è molto semplice:  
```hugo ```
Questo costruirà una cartella **public** nella directory principale del sito. Questo è il contenuto finale che andrà caricato online.
