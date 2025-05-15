---
layout: page
title: Lien d'évitement
permalink: lien-evitement.html
---

Un lien d’évitement du type « Aller au contenu » doit systématiquement être présent sur chaque page afin de faciliter la navigation au clavier. Si ce lien n'est pas présent, une personne navigant la page à l'aide d'un clavier devra "traverser" tous les menus avant d'arriver au contenu. Les liens d’évitement sont avant tout proposés pour les utilisateurs clavier (personnes déficientes motrices, par exemple).

En anglais, on parle de "Skip links". C'est le critère 2.4.1 (*Bypass Blocks*) du règlement WCAG.

Exemple simple donné par AcceDe Web:

```html
<body>
  <a class="evitement" href="#contenu">Aller au contenu</a>
  […]
  <main role="main" id="contenu">
     […]
  </main>
  […]
</body>
```

On peut masquer ce lien, on le positionne hors champ en lui donnant une position absolue, et une valeur "left" négative:

```css
a.evitement {
   display: inline-block;
   color: #555;
   background: #fff;
   padding: .5em;
   position: absolute;
   left: -99999rem;
   z-index: 100;
}
```

Pour le rendre visible lors de la navigation au clavier, on ajoute la règle suivante qui réagit au "focus". Le focus s'active si on navigue sur un élément avec le bouton "tab".

```css
a.evitement:focus {
   left: 0;
}
```

## Ressources

* [Mettre en place un lien d’évitement](https://www.accede-web.com/notices/html-et-css/navigation-au-clavier/mettre-en-place-un-lien-devitement/), Les notices AcceDe Web
* Article détaillé : [Les bonnes pratiques pour les liens d’évitements](https://a11y-guidelines.orange.com/fr/articles/liens-evitement/), Accessibilité Numérique Orange
* [Skip Link - Easy Checks](https://www.w3.org/WAI/test-evaluate/easy-checks/skip-link/), Web Accessibility
Initiative WAI
* [Bypass Blocks: Understanding SC 2.4.1](https://www.w3.org/WAI/WCAG22/Understanding/bypass-blocks.html), WCAG 2.2 Understanding Docs
