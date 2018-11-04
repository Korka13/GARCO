---
title: "MyNotepad"
date: 2018-09-15T18:29:43+03:00
draft: true
image: ""
categories: [""]
keywords: []
description: "Srivo qui le mie note/ lascia in draft"
weight: -6
---

css trick checkbox:
https://codersblock.com/blog/checkbox-trickery-with-css/
-----------------------




https://css-tricks.com/the-checkbox-hack/

consigli per zoom:
https://stackoverflow.com/questions/17844178/styling-multiple-checkboxes-with-css-is-not-working

https://stackoverflow.com/questions/13630229/can-i-have-an-onclick-effect-in-css

questo il meglio:
https://stackoverflow.com/questions/21479102/how-to-add-zoom-in-out-on-click-to-all-img-html-tags
====
.zoom-photo {
    transition: -webkit-transform 0.25s ease;
}

.zoom-photo:hover{
  cursor: zoom-in;
}
.zoom-photo:active {
    -webkit-transform: scale(2);
}

.zoom-photo:checked + label > img {
  size: 2;
}
====

https://stackoverflow.com/questions/39858998/zoom-in-and-out-on-mouse-click-with-css/39859268


zoom image with CSS:

HTML:
<div class="containerzoom">
  <input type="checkbox" id="zoomCheck">
  <label for="zoomCheck">
    <img src="/img/new-site.JPG">
  </label>
</div>

CSS:

input[type=checkbox] {
  display: none;
}

.containerzoom img {
  margin: 10px;
  transition: transform 0.25s ease;
  cursor: zoom-in;
}

input[type=checkbox]:checked ~ label > img {
  transform: scale(2);
  cursor: zoom-out;
}


------------------------

drive to web non funziona:

immagine open new page:
<a href="/img/win10variables.JPG" target="&#95;blank">
<img src="/img/win10variables.JPG" alt="Windows 10 variabili di ambiente">
</a>

link blank:

**<a href="https://heidoc.net/joomla/" target="_blank">HeiDoc.net</a>**

<a href="https://git-scm.com/download/win" target="&#95;blank">Homepage del sito</a>



Il tema quando l'ho scaricato io:
https://github.com/appernetic/hugo-nederburg-theme/tree/e21fa2492ed7fc58ab954d311f83339ea5fb50cb


git per windows : https://git-scm.com/download/win

install git: https://hackernoon.com/install-git-on-windows-9acf2a1944f0



----
# css per data ultimo aggiornamento
.updated-date-article {
  font-size: 0.813em;
  line-height: 1.85;
  text-transform: none;
  letter-spacing: 0.08em;
  font-weight: 700;
  color: #aaaaaa;
  padding-top: 1.84502em;
  padding-top: 3.69004em;
  text-align: center;
  padding-left: 5.55%;
  padding-right: 5.55%;
  font-size: 1em;
  line-height: 1.5;
  padding-top: 3em;
  letter-spacing: 0.08em;
}

@media all and (min-width: 68.75em) {
  .updated-date-article {
    padding-left: 11.11%;
    padding-right: 11.11%;
  }


.updated-date-article a {
  color: #aaaaaa;
}


.updated-date-article a:link, .updated-date-article a:visited {
  color: #aaaaaa;

}


.updated-date-article a:hover, .updated-date-article a:active, .updated-date-article a:focus {
  color: #38312f;
}
----

# il css background da compete themes, che però se applicato fa sparire hompage articolo background da mobile only:
body,
.excerpt,
.main,
.menu-primary ul,
#site-header {
	background: #444444;
}
#menu-primary-items a,
#title-info a {
	color: #FFFFFF;
}
.menu-secondary-items a,
.menu-secondary-items a:link,
.menu-secondary-items a:visited {
  color: #ffffff;
}
---
