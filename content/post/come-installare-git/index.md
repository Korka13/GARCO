---
title: "Come Installare Git"
date: 2018-09-15T22:50:02+03:00
lastmod:
draft: false
image: "img/git.jpg"
categories: ["WEB"]
keywords: [Installare Git su Windows, Scarica Git,]
description: "Git è uno dei più famosi sistemi di controllo versione distribuito. In questa guida andremo a installare Git su Windows in maniera molto basica in quanto questo articolo è solo parte di una guida più grande il cui obiettivo è costruire un sito web, e non l'utilizzo di Git come software."
weight: -31
---
*[Vai all'Indice completo della guida su come creare un sito come questo](/post/come-costruire-questo-blog-a-costo-zero-indice/)*

**Git** è uno dei più famosi *sistemi di controllo versione distribuito*. La sua funzione principale è quella di mantenere traccia delle modifiche apportate a un codice di programmazione nelle varie versioni. È utile ai programmatori per poter cooperare senza necessità di un server centrale. Per curiosità, è stato sviluppato nel 2005 da Linus Torvalds, il "papà" di Linux.

Per lo scopo che abbiamo in questo gruppo di post; creare un sito web usando Hugo, Git ci servirà solo per avere una maggiore comodità nello scaricare temi e file da **GitHub**, quindi faremo un'installazione molto basica.  
Anche Git esiste per tutte le piattaforme, io per il momento spiegherò l'installazione su Windows, <a href="https://git-scm.com/download/win" target="&#95;blank">questa è la pagina di download</a>.  
Aperta la pagina dovrebbe partire in automatico il download della versione a 64bit, se non parte o se vi serve quella a 32bit cliccate su quella che vi serve ed eseguite il file.  
Come accennavo Git è un programma abbastanza complesso, ma per l'intento di questa guida servirà a poco, quindi tutte le impostazioni consigliate predefinite andranno bene. Potete cliccare avanti avanti finché non sono finite (ce ne sono un bel po'). Annotate soltanto il path dove viene installato il pacchetto di Git, se servisse aggiungerlo alle variabili di ambiente.  
Una volta terminata l'installazione aprite una finestra del prompt dei comandi ed eseguite:  
```git --version```  
Se viene riportata la versione installata di Git è tutto a posto, mentre se riporta un errore dovrete aggiungere il percorso di cui avete preso nota durante l'installazione e aggiungerlo alle variabili di ambiente esattamente come è stato fatto quando abbiamo installato [Hugo](/post/come-installare-hugo/).  

[Per il momento Git lo lasciamo da parte, e andiamo a creare la struttura del sito.](/post/struttura-della-directory-del-sito-su-hugo/)

**Grazie!**
