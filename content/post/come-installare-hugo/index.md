---
title: "Come Installare HUGO"
date: 2018-09-09T04:48:55+03:00
lastmod: 2018-09-15
draft: false
image: "img/hugo.png"
categories: ["WEB"]
keywords: [Hugo, Windows, Static Website Generator, Install]
description: "HUGO static website generator è uno strumento per creare appunto siti web statici, questa guida spiega passo passo come installarlo su un computer Windows"
weight: -40
---
*[Vai all'Indice completo della guida su come creare un sito come questo](/post/come-costruire-questo-blog-a-costo-zero-indice/)*  

**HUGO**: innanzitutto, che cos'è? È un programma, è disponibile praticamente per qualsiasi piattaforma, io per il momento spiegherò passo passo come installarlo su Windows, se avete Mac OS ci sono molte guide in inglese online (<a href="https://www.youtube.com/watch?v=WvhCGlLcrF8" target="&#95;blank">qui un video</a>), se avete Linux non credo vi serva il mio aiuto.  
Il programma aiuta a creare un sito web statico, ovvero che non ha parti dinamiche come PHP, ma si basa solo su HTML, JavaScript e CSS. Questo lo rende più veloce di uno dinamico in quanto è più semplice accedere a ogni risorsa, e lo rende più protetto dall'essere infettato da virus, perché ogni volta che il contenuto cambia, va cancellato e ricaricato completamente sul server. HUGO non ha un'interfaccia GUI, si usa dal Command Prompt o dal Terminal, crea le cartelle e i file necessari alla costruzione del sito, e poi trasforma tutto in HTML dandoci una cartella pronta da caricare sul server, il nostro sito.

* Per prima cosa scarica il file zip da <a href="https://github.com/gohugoio/hugo/releases" target="&#95;blank">questa pagina</a> hugo_000_Windows-64bit.zip oppure il 32bit in base al pc, ed estrai il contenuto in C:\Hugo\bin (dovrebbero esserci 3 file, hugo.exe, ).  
* Apri una finestra di command prompt e scrivi:  

`cd C:\Hugo\bin`   
`hugo version`

* Se l'output è qualcosa come `Hugo Static Site Generator v0.47.1 windows/amd64 BuildDate: 2018-08-20T08:17:26Z`, Hugo è installato e funziona, altrimenti c'è qualcosa che non va.  
* Ora, dobbiamo modificare un settaggio di Windows per fare in modo che i comandi di Hugo funzionino in qualunque posizione, non solo in C:\Hugo\bin, per farlo, andiamo ad aggiungere il percorso nelle variabili di ambiante di percorso: ricerca su Windows: variabili d'ambiente e scegli *"modifica le variabili d'ambiente del sistema"* poi dalla scheda "Proprietà di Sistema" -> "Variabili d'ambiente" -> "PATH"
* Se hai Winodws 10 aggiungi il percorso `C:\Hugo\bin` in una nuova riga, se hai Windows 7 aggiungi `;C:\Hugo\bin` dopo quello che c'è già scritto:  
Scrrenshots:  

<div class="container">
  <input type="checkbox" id="zoomCheck">
  <label for="zoomCheck">
    <img src="/img/win7variables.JPG">
  </label>
</div>

<div class="container">
  <input type="checkbox" id="zoomCheckCheck">
  <label for="zoomCheckCheck">
    <img src="/img/win10variables.JPG">
  </label>
</div>

Questo è tutto per quanto riguarda l'installazione di Hugo.  

[Leggi come installare Atom text editor](/post/come-installare-atom-text-editor)

**Grazie!**
