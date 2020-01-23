# Checklist intégration d'emails 🔥⚔️

L'objectif de cette checklist est de regrouper de manière condensée l'essentiel de ce qu'il faut retenir pour réaliser des intégrations d'emails responsive de manière moderne.

Influances menant à cette checklist :

- [FrontEnd Masters Course on html email development V2](https://frontendmasters.com/courses/html-email-v2)

## Petit rappel de ce qui devrait marcher, et ne pas marcher du tout

Ce qui devrait marcher :

- HTML Basique
- CSS basique
  - pour le texte : `color`, `font-family`, `font-size`, `font-style`, `font-weight`, `line-height`, `text-align`
  - pour les blocs : `margin`, `padding`, `width`, `max-width`, `border`
- Layout basé sur les tableaux
- Sémantique simple

Ce qui ne marchera surement pas :

- Positionnement `float`
- CSS Grid
- JavaScript
- Beaucoup de CSS

## Starter

Pour bien démarrer, utilisez le fichier `template.html` qui fournira une base solide.

Prenez bien garde aux commentaires html inclus à l'intérieur, ils préciseront des points de détails importants qui ne seront pas donnés dans ce document.

## Quelques règles de base

- [ ] 14px minimum pour tout contenu textuel (oui, même les infos légales, lien de désinscription etc.)
- [ ] pour le contenu, vos balises préférées seront `div`, `span`, `h1` à `h6`, `p`, `strong`, `em` et `img`
- [ ] pour la structure et le positionnement, faites la paix avec `table`
- [ ] utiliser le `px` pour toutes les unités de mesure
- [ ] ne pas utiliser des images pour les boutons
