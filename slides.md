---
# try also 'default' to start simple
theme: seriph
colorSchema: dark
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: "text-center"
# https://sli.dev/custom/highlighters.html
highlighter: shiki
# show line numbers in code blocks
lineNumbers: false
# some information about the slides, markdown enabled
info: |
  ## Slidev Starter Template
  Presentation slides for developers.

  Learn more at [Sli.dev](https://sli.dev)
# persist drawings in exports and build
drawings:
  persist: false
---

# A la découverte de Nuxt 3 ⭐

<div class="abs-br m-6 flex gap-2">
  <button @click="$slidev.nav.openInEditor()" title="Open in Editor" class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon:edit />
  </button>
  <a href="https://github.com/slidevjs/slidev" target="_blank" alt="GitHub"
    class="text-xl icon-btn opacity-50 !border-none !hover:text-white">
    <carbon-logo-github />
  </a>
</div>

<!--
The last comment block of each slide will be treated as slide notes. It will be visible and editable in Presenter Mode along with the slide. [Read more in the docs](https://sli.dev/guide/syntax.html#notes)
-->

---

# A propos de moi

--

<v-click>

- développeuse freelance front-end (Vue, Angular)
- instructrice LinkedIn Learning

</v-click>

<v-click>

- meetup Nuxt : https://www.meetup.com/meetup-group-nuxt/

</v-click>

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

<div class="container">
  <h1 class="selected">1. Qu'est-ce que Nuxt ?</h1>
  <h1>2. Nuxt 3</h1>
</div>

<style>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
}
.selected {
  color: #dbf5ff
}
</style>

---

# Nuxt: définition

--

<v-clicks>

<div style="margin-bottom: 15px">Méta-framework basé sur Vue.</div>

_Nb: metaframework = framework écrit sur un autre framework_

<img style="height: 200px;" src="images/wtc.PNG" />

</v-clicks>

---

# Nuxt: définition

--

<div style="margin-bottom: 15px">Méta-framework basé sur Vue.</div>

<!-- Component usage: this will be invisible until you press "next" -->
<v-clicks>

> "To me, that sounds like React is a kernel [...] Next.js and Gatsby are the closest things we've got to distros."
>
> James K Nelson

> _=> adaptable à l'éco-système Vue (Nuxt, Quasar, Gridsome...)_

</v-clicks>

---

# Et qu'apporte Nuxt (hors v3) ?

--

<v-clicks>

Vue : "Le Framework JavaScript Évolutif" _=> UI runtime (+ routing et state management non imposés)_

</v-clicks>

---

# Et qu'apporte Nuxt (hors v3) ?

--

<v-clicks style="padding: 0px 0 10px 0">

- Bootstrap facilité: préconfiguration, conventions\* (structure de dossiers)
- Expérience developpeur : routing (+ state management) par système de fichiers, auto-import des composants
- Modes de rendus : SSR et SSG (+ outils associés) _=> amélioration performances (**TTC** et **SEO**)_

</v-clicks>

<v-click>

\* _Nuxt reste relativement peu 'opinionated' car la plupart des implémentations sont configurables._

</v-click>

---

# SSR et SSG
--

<v-clicks>

Bootstrap d'une SPA dans un navigateur : 

<svg style="left: 0px; top: 0px; width: 100%; height: 100%; display: block; min-width: 795px; min-height: 165px; background-color: transparent; background-image: none;"><defs><filter id="dropShadow"><feGaussianBlur in="SourceAlpha" stdDeviation="1.7" result="blur"></feGaussianBlur><feOffset in="blur" dx="3" dy="3" result="offsetBlur"></feOffset><feFlood flood-color="#3D4574" flood-opacity="0.4" result="offsetColor"></feFlood><feComposite in="offsetColor" in2="offsetBlur" operator="in" result="offsetBlur"></feComposite><feBlend in="SourceGraphic" in2="offsetBlur"></feBlend></filter></defs><g transformOrigin="0 0" transform="scale(1,1)translate(-82,-337)"><g></g><g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 110 420 L 753.63 420" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 110 420 L 753.63 420" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 758.88 420 L 751.88 423.5 L 753.63 420 L 751.88 416.5 Z" fill="#ffffff" stroke="#ffffff" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 760 460 L 760 436.37" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 760 460 L 760 436.37" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 760 431.12 L 763.5 438.12 L 760 436.37 L 756.5 438.12 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="280" y="420" width="310" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="280" y="420" width="310" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 435px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement ressources (JS, assets...)</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 640 430 L 640 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 640 430 L 640 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="650" y="420" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="650" y="420" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 695px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Bootstrap</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="710" y="455" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="710" y="455" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 470px; margin-left: 755px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">TTC* + TTI**</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="770" y="405" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="770" y="405" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 420px; margin-left: 815px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">SPA ready</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 430 L 230 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 430 L 230 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="120" y="420" width="110" height="50" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="120" y="420" width="110" height="50" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 445px; margin-left: 175px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement <br>HTML initial</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 375 L 230 398.63" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 375 L 230 398.63" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 230 403.88 L 226.5 396.88 L 230 398.63 L 233.5 396.88 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="90" y="345" width="290" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="90" y="345" width="290" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 360px; margin-left: 235px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">Affichage index.html (point d'entrée)</div></div></div></foreignObject></g></g></g><g></g><g></g></g></svg>

\* *TTC = Time To Content (affichage du contenu de la page lors de la première requête)*

\*\* *TTI = Time To Interaction (SPA fonctionnelle)*


<div style="padding: 20px 0 10px 0">=> Objectif SSR (et SSG): diminuer le TTC (+ améliorer SEO)</div>

</v-clicks>

---

# SSR et SSG
--

<v-clicks>

SSR d'une SPA : 

<svg style="left: 0px; top: 0px; width: 100%; height: 100%; display: block; min-width: 936px; min-height: 170px; background-color: transparent; background-image: none;"><defs><filter id="dropShadow"><feGaussianBlur in="SourceAlpha" stdDeviation="1.7" result="blur"></feGaussianBlur><feOffset in="blur" dx="3" dy="3" result="offsetBlur"></feOffset><feFlood flood-color="#3D4574" flood-opacity="0.4" result="offsetColor"></feFlood><feComposite in="offsetColor" in2="offsetBlur" operator="in" result="offsetBlur"></feComposite><feBlend in="SourceGraphic" in2="offsetBlur"></feBlend></filter></defs><g transformOrigin="0 0" transform="scale(1,1)translate(59,-337)"><g></g><g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 121.36 417.97 L 753.63 419.98" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 121.36 417.97 L 753.63 419.98" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 758.88 420 L 751.87 423.47 L 753.63 419.98 L 751.89 416.47 Z" fill="#ffffff" stroke="#ffffff" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 760 460 L 760 436.37" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 760 460 L 760 436.37" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 760 431.12 L 763.5 438.12 L 760 436.37 L 756.5 438.12 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="280" y="420" width="310" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="280" y="420" width="310" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 435px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement ressources (JS, assets...)</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 640 430 L 640 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 640 430 L 640 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="650" y="420" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="650" y="420" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 695px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Bootstrap</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="735" y="455" width="40" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="735" y="455" width="40" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 470px; margin-left: 755px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">TTI</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="770" y="405" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="770" y="405" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 420px; margin-left: 815px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">SPA ready</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 430 L 230 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 430 L 230 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="120" y="420" width="110" height="70" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="120" y="420" width="110" height="70" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 455px; margin-left: 175px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement <br>HTML page <br>requêtée</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 375 L 230 398.63" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 375 L 230 398.63" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 230 403.88 L 226.5 396.88 L 230 398.63 L 233.5 396.88 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="210" y="345" width="50" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="210" y="345" width="50" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 360px; margin-left: 235px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">TTC</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 119 430 L 119 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 119 430 L 119 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="-50" y="420" width="170" height="70" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="-50" y="420" width="170" height="70" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 455px; margin-left: 35px;"><div data-drawio-colors="color: #99CCFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(153, 204, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Génération sur&nbsp;<br>serveur du HTML de <br>la page requêtée</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M -51.36 418.81 L 120 419" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M -51.36 418.81 L 120 419" fill="none" stroke="#99ccff" stroke-miterlimit="10" stroke-dasharray="3 3" pointer-events="stroke"></path></g></g><g></g><g></g></g></svg>

Avantages :
- faible TTI
- meilleur SEO

Mais : moins scalable

</v-clicks>

---

# SSR versus SSG
--

<v-clicks>

SSR avec opération serveur:

<svg style="left: 0px; top: 0px; width: 100%; height: 100%; display: block; min-width: 1095px; min-height: 165px; background-color: transparent; background-image: none; transform: scaleX(0.85) translateX(-10%)"><defs><filter id="dropShadow"><feGaussianBlur in="SourceAlpha" stdDeviation="1.7" result="blur"></feGaussianBlur><feOffset in="blur" dx="3" dy="3" result="offsetBlur"></feOffset><feFlood flood-color="#3D4574" flood-opacity="0.4" result="offsetColor"></feFlood><feComposite in="offsetColor" in2="offsetBlur" operator="in" result="offsetBlur"></feComposite><feBlend in="SourceGraphic" in2="offsetBlur"></feBlend></filter></defs><g transformOrigin="0 0" transform="scale(1,1)translate(198,-342)"><g></g><g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 131.36 417.97 L 753.63 419.98" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 131.36 417.97 L 753.63 419.98" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 758.88 420 L 751.87 423.47 L 753.63 419.98 L 751.89 416.47 Z" fill="#ffffff" stroke="#ffffff" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 760 460 L 760 436.37" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 760 460 L 760 436.37" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 760 431.12 L 763.5 438.12 L 760 436.37 L 756.5 438.12 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="280" y="420" width="310" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="280" y="420" width="310" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 435px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement ressources (JS, assets...)</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 640 430 L 640 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 640 430 L 640 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="650" y="420" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="650" y="420" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 435px; margin-left: 695px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Bootstrap</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="620" y="460" width="260" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="620" y="460" width="260" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 475px; margin-left: 750px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">TTI (avec données dynamiques)</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="770" y="405" width="90" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="770" y="405" width="90" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 420px; margin-left: 815px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">SPA ready</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 430 L 230 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 430 L 230 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="120" y="420" width="110" height="70" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="120" y="420" width="110" height="70" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 455px; margin-left: 175px;"><div data-drawio-colors="color: #FFFFFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 255, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Chargement <br>HTML page <br>requêtée</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 230 375 L 230 398.63" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 230 375 L 230 398.63" fill="none" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="stroke"></path><path d="M 230 403.88 L 226.5 396.88 L 230 398.63 L 233.5 396.88 Z" fill="#ffcc99" stroke="#ffcc99" stroke-miterlimit="10" pointer-events="all"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="100" y="350" width="270" height="30" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="100" y="350" width="270" height="30" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 365px; margin-left: 235px;"><div data-drawio-colors="color: #FFCE9F; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(255, 206, 159); line-height: 1.2; pointer-events: all; white-space: nowrap;">TTC (avec données dynamiques)</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M 119 430 L 119 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M 119 430 L 119 410" fill="none" stroke="#ffffff" stroke-miterlimit="10" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="-40" y="420" width="170" height="70" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="-40" y="420" width="170" height="70" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 455px; margin-left: 45px;"><div data-drawio-colors="color: #99CCFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(153, 204, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Génération sur&nbsp;<br>serveur du HTML de <br>la page requêtée</div></div></div></foreignObject></g></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M -190 419 L 120 419" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M -190 419 L 120 419" fill="none" stroke="#99ccff" stroke-miterlimit="10" stroke-dasharray="3 3" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><path d="M -40 430 L -40 410" fill="none" stroke="white" stroke-miterlimit="10" pointer-events="stroke" visibility="hidden" stroke-width="9"></path><path d="M -40 430 L -40 410" fill="none" stroke="#99ccff" stroke-miterlimit="10" stroke-dasharray="3 3" pointer-events="stroke"></path></g><g transform="translate(0.5,0.5)" style="visibility: visible;"><rect x="-180" y="420" width="140" height="50" fill="none" stroke="white" pointer-events="stroke" visibility="hidden" stroke-width="9"></rect><rect x="-180" y="420" width="140" height="50" fill="none" stroke="none" pointer-events="all"></rect></g><g style=""><g><foreignObject pointer-events="none" width="100%" height="100%" style="overflow: visible; text-align: left;"><div style="display: flex; align-items: unsafe center; justify-content: unsafe center; width: 1px; height: 1px; padding-top: 445px; margin-left: -110px;"><div data-drawio-colors="color: #99CCFF; " style="box-sizing: border-box; font-size: 0px; text-align: center;"><div style="display: inline-block; font-size: 17px; font-family: Helvetica; color: rgb(153, 204, 255); line-height: 1.2; pointer-events: all; white-space: nowrap;">Récupération de <br>données en DB</div></div></div></foreignObject></g></g></g><g></g><g></g></g></svg>

</v-clicks>

---

# SSR versus SSG
--

<v-clicks>

SSG d'une SPA :

// todo

</v-clicks>

---
layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080
---

<div class="container">
  <h1>1. Qu'est-ce que Nuxt ?</h1>
  <h1 class="selected">2. Nuxt 3</h1>
</div>

<style>
.container {
  display: flex;
  flex-direction: column;
  justify-content: center;
  height: 100%;
}
.selected {
  color: #dbf5ff
}
</style>

---

# Context global

<v-click>

_cf Daniel Roe, Edge-rendering with Nuxt, Vuejs Amsterdam 2021_

</v-click>

<v-clicks style="padding: 30px 0 10px 0">

- Serverless : déléguer la gestion et la dimension des infrastructures serveur à un service Cloud
- Jamstack (JavaScript Api Markup) : 'pre-rendering' et découplage (microservices) => applications plus rapides, sécurisées et scalables.

</v-clicks>

<v-clicks style="padding: 10px 0 10px 0">

- nouvelles 'targets' : Deno, workers

</v-clicks>

<v-clicks style="padding: 10px 0 10px 0">

- TypeScript
- ES modules : portée par nouveaux outils de développements (Vite, Snowpack)

</v-clicks>

---

Nuxt :

- v2 : "Le framework Vue intuitif"
- v3 : "The hybrid Vue framework"

---

# Nuxt 3 : support

<v-clicks style="padding: 30px 0 10px 0">

- TypeScript : types auto-générés (composants globaux, composables, routes API...)
- Vue 3 : API de composition (dossier 'composables', auto-imports), API suspense
- Bundler : Webpack 5, Vite
- Transpiler : esbuild
- State management : `useState`

</v-clicks>

---

# Nuxt 3 : expérience développeur

<v-click style="padding: 30px 0 10px 0">

<Tweet id="1451192466049093633" scale="0.65" />

</v-click>

---

# Nuxt 3 : 'big features'

<v-clicks style="padding: 30px 0 10px 0">

- Nuxt Kit : modules cross-version
- CLI : Nuxi
- Dev tools (à venir)
- Rendering server : Nitro 🔥 (basé sur le serveur h3 du repository unjs)

</v-clicks>

---

# Nuxt 3 : Nitro 🔥

<v-click >

<div style="padding: 30px 0 10px 0">Features :</div>

</v-click>
<v-clicks style="padding: 0px 0 0px 0">

- server API (génération automatique de types)
- mode hybride : SSR et SSG

</v-clicks>

<v-click>

<div style="padding: 30px 0 10px 0">Universel :</div>

</v-click>

<v-clicks style="padding: 0px 0 0px 0">

- build multi-targets: Node, Deno, workers (serverless, expérimentalement sur navigateur)

</v-clicks>

<v-click>

<div style="padding: 30px 0 10px 0">Construit pour le serverless :</div>

</v-click>

<v-clicks style="padding: 0px 0 0px 0">

- détection automatique des plateformes serverless (Netlify, Vercel, Azure, AWS, and CloudFlare Workers)
- cold start optimisé
- plus léger (NFT)

</v-clicks>

---

layout: image-right
image: https://source.unsplash.com/collection/94734566/1920x1080

---

# Conclusion

<v-click>

<div style="padding: 30px 0 10px 0">Nuxt semble avoir pris un tournant avec cette version 3, et dépasse le 'meta-framework' Vue pour se positionner plutôt comme 'an open source framework making web development simple and powerful'.</div>

</v-click>
