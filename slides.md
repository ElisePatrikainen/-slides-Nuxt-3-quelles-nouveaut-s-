---
# try also 'default' to start simple
theme: seriph
# random image from a curated Unsplash collection by Anthony
# like them? see https://unsplash.com/collections/94734566/slidev
background: https://source.unsplash.com/collection/94734566/1920x1080
# apply any windi css classes to the current slide
class: 'text-center'
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

# Nuxt 3, quelles nouveautés ?

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

<v-click>

- développeuse freelance front-end (Vue, Angular) en mission chez Vesperia
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

<!-- Component usage: this will be invisible until you press "next" -->
<v-click>

- v2: "Le framework Vue intuitif"

</v-click>

<v-click>

- v3: "The Hybrid Vue Framework"

</v-click>

<v-click>

=> meta-framework basé sur Vue

</v-click>

---

# Contexte

<div style="padding: 30px 0">
<v-click>

- front-end

</v-click>

<v-click>

- SPA

</v-click>
</div>

<div>
<v-click>

Dominé par :

</v-click>

<v-clicks>

<ul>
<li>Angular</li>
<li>React</li>
<li>Vue</li>
<li class="medium">Svelte</li>
<li class="small">Riot</li>
<li class="small">Solid</li>
</ul>

</v-clicks>
</div>

<style>

.medium {
  opacity: 60%
}
.small {
  opacity: 40%
}
</style>

---

# Pourquoi des meta-frameworks ?

<v-clicks style="padding: 30px 0">

- Angular : "The modern web developer's platform" *=> langage, directory structure, UI runtime, routing, formulaires, client HTTP, tests...*
- React : "Une bibliothèque JavaScript pour créer des interfaces utilisateurs" *=> UI runtime*
- Vue : "Le Framework JavaScript Évolutif" *=> UI runtime + routing et state management non imposés*

</v-clicks>

<v-click>

=> React et Vue : grand flexibilité, mais difficultés pour bootstrap et implémentation de features clés (SSR, ...)

</v-click>

---

# Pourquoi des meta-frameworks ?

<v-clicks style="padding: 30px 0">

- React : Next, Gatsby (SSG)
- Vue : Nuxt, Quasar, Gridsome (SSG)

</v-clicks>

<v-click>

>"To me, that sounds like React is a kernel. Webpack/Create React App are bootloaders. Next.js and Gatsby are the closest things we've got to distros."
>
>James K Nelson

</v-click>

---

# Nuxt (hors v3)


<v-click>

<div style="padding: 30px 0 10px 0">Préconfiguration :</div>

</v-click>

<v-clicks style="padding: 0px 0 10px 0">

- Conventions : structure de dossiers 
- Bootstrap : pré-intégration du router, de Vuex (Nuxt 2) et du **SSR**

</v-clicks>


<v-click>

<div style="padding: 20px 0 10px 0">Features :</div>

</v-click>
<v-clicks style="padding: 0px 0 10px 0">

- Expérience developpeur : routing (+ state management) par système de fichiers, auto-import des composants
- Modes de rendus : SSG, outils (hooks) *=> amélioration de **TTC** et **SEO** par pre-rendering HTML et pre-fetch de data, architecture Jamstack*

</v-clicks>

<v-click>

*Nb: Nuxt reste relativement peu 'opinionated' car la plupart des implémentations sont configurables.*

</v-click>

---

# SSR et SSG

<v-click>

<div style="padding: 20px 0 10px 0">Objectif: diminuer le TTC d'une SPA (+ améliorer SEO)</div>

</v-click>


<v-click>

<div style="padding: 20px 0 10px 0; font-style: italic; color: grey">Nb: TTC = Time To Content (affichage du contenu de la page lors de la première requête)</div>

</v-click>


<v-click>

<div style="padding: 20px 0 10px 0; font-style: italic; color: grey">Nb2: SPA ont un fort TTC (et un SEO potentiellement diminué) car le contenu de la page d'une SPA n'est visible qu'une fois la SPA chargée (temps, notemment sur faible réseau)</div>

</v-click>

---

# SSR et SSG

<v-click>

<div style="padding: 20px 0 10px 0">Comment? utiliser le serveur pour :</div>

</v-click>

<v-clicks style="padding: 0px 0 10px 0">

- pré-rendre le contenu de la page
- 'pre-fetcher' les datas (plutôt que de le faire dans un second temps de façon asynchrone)

</v-clicks>

---

# SSR versus SSG

<v-clicks style="padding: 0px 0 10px 0">

- SSR : pré-rendering au run-time *=> flexibilité*
- SSG : pré-rendering au build *=> architecture Jamstack, scalabilité (fichiers statiques, fetch data réduit)*

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

*cf Daniel Roe, Edge-rendering with Nuxt, Vuejs Amsterdam 2021*

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

