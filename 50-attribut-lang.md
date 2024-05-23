---
layout: page
title: Attribut de Langue
permalink: attribut-langue.html
---
La présence d'un attribut indiquant la langue de la page est requise pour la confirmité WCAG de niveau A. Sans cet attribut, un logiciel de lecture ne saura pas comment prononcer correctement le contenu.

Voici comment renseigner l'attribut "lang", sur la balise "html" tout au début du document:

```html
<!doctype html>
<html lang="fr"> 
<head>
  <meta charset="utf-8">
  <title>document écrit en français</title>
</head>  
<body>     
  ... document écrit en français ...
</body>
</html>
```

Voir: WCAG Success Criterion 3.1.1 [Language of Page](https://www.w3.org/WAI/WCAG22/Understanding/language-of-page)