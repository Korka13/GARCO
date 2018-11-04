---
title: "Struttura della Directory del Sito su Hugo"
date: 2018-09-16T21:59:47+03:00
lastmod:
draft: false
image: "img/folder-tree.jpg"
categories: ["WEB"]
keywords: [Hugo, Directory, Struttura, Creare il sito, Toml]
description: "Hugo static website generator per prima cosa permette di creare la struttura con il comando predefinito. Creaiamo la prima struttura e vediamo a cosa servono le varie cartelle che vengono create al suo interno"
weight: -30
---
*[Vai all'Indice completo della guida su come creare un sito come questo](/post/come-costruire-questo-blog-a-costo-zero-indice/)*

Allora, partiamo dal decidere dove verrà creato il sito. In diverse guide che ho trovato, quando si installa Hugo, danno indicazione di creare due cartelle, una **"bin"**, che abbiamo creato anche noi, e una **"Sites"**, che invece io non ho menzionato nella guida.
Non l'ho menzionata perché non l'ho trovata necessaria, potete tenere i siti dove vi è più comodo. Io per esempio li tengo su una chiavetta USB per due motivi; primo posso portarmela a lavoro e continuare da li (che sarebbe anche bypassabile riscaricando i backup da OneDrive), e secondo perché un sito web statico viene sempre cancellato per poi essere ricreato, ad ogni modifica, quindi avendo un SSD credo che potrebbe rovinarsi più facilmente.
Quindi, semplicemente create una cartella **Sites** dove preferite, l'unico consiglio che vi do è di mantenere corto il path, in quanto lavorando da linea di comando può essere scomodo lavore con il path troppo lungo; per esempio, create **C:\Sites** o **C:\Hugo\Sites**, nel mio caso parliamo du una chiavetta esterna quindi **E:\Sites**.

Ora apriamo Atom, e il terminal al suo interno cliccando sul + in basso a sinistra.
Dal terminal dobbiamo entrare nella cartella Sites che abbiamo creato usando il comando *cd [spazio] [percorso della cartella]*, per esempio:

```cd C:\Sites```
o:
```cd C:\Hugo\Sites```
oppure:
```cd E:\Sites```

Una volta nella cartella desiderata il comando per creare la struttura del sito è *hugo new site [nome del sito]*, per esempio:

```hugo new site NewSite```

Ora la cartella contente il sito è stata creata. Da Atom -> File -> Add Project Folder selezioniamo la cartella NewSite (o come è stata chiamata nel comando precedente) e diamo un'occhiata veloce alle sottocartelle e i file:


<div class="container">
  <input type="checkbox" id="zoomCheckCheck">
  <label for="zoomCheckCheck">
    <img src="/img/new-site.JPG">
  </label>
</div>

````
E:.
│   config.toml
│
├───layouts
├───content
├───archetypes
│       default.md
│
├───static
├───data
└───themes
````
### config.toml
Questo file è essenziale per ogni sito di Hugo, all'interno verranno inserite diverse istruzioni che Hugo leggerà e interpreterà per cosatruire il sito. in base a cosa si vuole ottenere ci sono molte indicazioni che si possono dare. Per esempio, tramite questo file si istrurà Hugo su quale tema usare per il sito.
### Layouts
In questa cartella vengono inseriti file .html che Hugo userà per costruire il sito vero e proprio. Nel nostro caso vedrete che per esempio ci saranno file diversi in .htm per il footer, header, contenuto, etc etc, che Hugo poi combinerà tutti insieme per costruire le varie pagine del sito.
### Content
Qui verrà inserito tutto il contenuto del sito, ogni pagina viene scritta qui; la pagina contatti, informazioni, privacy, etc.. Le pagine al suo interno sono scritti in MarkDown (file .md) un linguaggio semplificato che poi Hugo trasforma in .html. Questo articolo per esempio è stato scritto nella cartella content/posts/struttura-della-directory-del-sito-su-hugo/index.md.
### Archetypes -> default.md
All'interno di questa cartella vengono tenute informazioni che indicano a Hugo come creare nuovo contenuto. Per esempio, in default.md possiamo aggiungere le informazioni che vogliamo che vengano già inserite automaticamente quando chidiamo a Hugo di creare un nuovo file MarkDown. Su questo approfondiremo in seguito.
### Static
In questa cartella vengono contenuti tutti i file che verrano portati sul sito da Hugo invariati, senza essere processati. Per esempio ci saranno le immagini, i file CSS e JavaScript.
### Data
Qui possono essere inseriti dai file in linguaggio TOML, YAML o JSON che servono come ulteriori templates a Hugo per generare il sito. Non è una cosa che approfondiremo in questa guida.
### Themes
Qui scaricheremo il tema del sito. Il tema conterrà anch'esso cartelle come quelle che abbiamo visto sopra. Una volta impostato il tema, se Hugo non troverà alcun layout in NewSite/layouts, li cercherà in NewSite/themes/theme/layouts.

[È il momento di scegliere un tema e installarlo sul nostro sito](/post/scaricare-il-tema-del-sito-su-hugo/)
