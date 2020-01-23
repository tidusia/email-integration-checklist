# Checklist intégration d'emails 🔥⚔️

L'objectif de cette checklist est de regrouper de manière condensée l'essentiel de ce qu'il faut retenir pour réaliser des intégrations d'emails responsive de manière moderne.

Influance(s) menant à cette checklist :

- [FrontEnd Masters Course on html email development V2](https://frontendmasters.com/courses/html-email-v2)

## Petit rappel de ce qui devrait marcher, et ne pas marcher du tout

Ce qui devrait marcher :

- HTML Basique
- CSS basique
  - pour le texte : `color`, `font-family`, `font-size`, `font-style`, `font-weight`, `line-height`, `text-align`
  - pour les blocs : `margin`, `padding`, `width`, `max-width`, `border`
- Layout basé sur les tableaux

Ce qui ne marchera surement pas :

- Positionnement `float`
- CSS Grid
- JavaScript
- Pas mal de CSS

## Starter

Pour bien démarrer, utilisez le fichier `template.html` qui fournira une base solide.

Prenez bien garde aux commentaires html inclus à l'intérieur, ils préciseront des points de détails importants qui ne seront pas donnés dans ce document.

## Boutons

Pour les boutons, les 2 meilleures approches sont les suivantes :

- Générer un buton en VML (artillerie lourde) sur [Buttons.cm](https://buttons.cm/)
- Utiliser la solution en example dans le `template.html` qui utilise du `table` + du padding et des bordures

## Images

- Toujours remplir l'attribut alt (sauf pour les éléments purement décoratifs sans aucune sémantique)
- Rester sur les formats traditionnels : `jpg`, `png`, `gif`
- Compresser les images au maximum pour limiter les ressources en bande passante de l'utilisateur
- Pour rendre une image responsive, suivez l'exemple dans le template (`img#responsive-image`)
- Si vous utilisez des background-images, pensez à ajouter une couleur de fond au cas où votre image ne serait pas chargée, comme dans le template (`#background-image`)
- Ne pas utiliser des images pour remplacer du contenu textuel difficile à styliser
- Et bien sur, utilisez des liens absolus (contrairement au template qui utilise les images du repo !)

## Accessibilité côté design

- Contraste de couleur élevé
- Rendre la hierarchie des informations claire au premier coup d'oeil
- La priorité : facilité de lecture (taille de police, espacements, hauteur de ligne, 14px minimum pour tout contenu textuel (oui, même les infos légales, lien de désinscription etc.))
- Autant que possible, conserver le standard visuel pour les liens : couleur différente et souligné. Et en bonus : `font-weight: bold`.
- Limiter le texte centré et justifié, surtout pour les paragraphes
- Limitez l'usage des images, elles sont très souvent bloquées par les clients mails ou les utilisateurs et consomment de la bande passante souvent inutilement. Votre contenu doit être principalement textuel, les images sont un bonus visuel. Un bon exemple d'utilisation d'image est le logo, avec un attribut alt. Un mauvais exemple : une image contenant du texte et des faux boutons.
- Garder une structure simple

## Accessibilité côté développement

- Pour le contenu, vos balises préférées seront `div`, `span`, `h1` à `h6`, `p`, `strong`, `em` et `img`
- Pour la structure et le positionnement, faites la paix avec `table`, oubliez les `thead`, `tbody` et `tfoot`. Place aux `tr` et `td` !
- Ajouter l'attribut `role="presentation"` aux éléments `table`
- Utiliser le `px` pour toutes les unités de mesure
- Ne pas utiliser des images pour les boutons, les liens et le contenu textuel
- L'attribut `lang` est très important. Bien penser à le mettre à jour pour chaque campagne internationnalisée. Si une (ou plusieures) partie distincte de votre document html est dans un autre langage, vous pouvez surcharger la langue localement en appliquant un autre attribut `lang` à cet élément précis.
- Même si la plupart des clients mails ne vont pas utiliser la balise `title`, il est intéressant de l'indiquer quand même car certaines personnes vont ouvrir et trier leurs emails dans un navigateur
- Vous pouvez choisir le texte qui sera utilisé en description d'email (sous la ligne d'objet), il s'agira du premier texte dans le body. Vous pouvez le masquer comme dans le template (`#description`).

## Ressources intéressantes

- [Litmus Community](https://litmus.com/community) : ensemble d'articles autour du sujet
- [Buttons.cm](https://buttons.cm/) : génération de bouttons à toute épreuve (mais code vraiment complexe)
- [NVDA](https://developer.paciellogroup.com/blog/2008/01/nvda-a-free-and-open-source-screen-reader-for-windows/) : lecteur d'écran pour windows
- [VoiceOver](https://help.apple.com/voiceover/mac/10.15/) : lecteur d'écran pour MacOS
- [NoCoffee](https://chrome.google.com/webstore/detail/nocoffee/jjeeggmbnhckmgdhmgdckeigabjfbddl?hl=en-US) : pour simuler des déficiences visuelles
- [Tota11y](https://chrome.google.com/webstore/detail/tota11y-plugin-from-khan/oedofneiplgibimfkccchnimiadcmhpe?hl=en) : pour vérifier la structure et la sémantique
- [SilkTide](https://silktide.com/) : pour auditer de nombreux aspects, va beaucoup plus loin que l'a11y
- [WAVE](https://wave.webaim.org/) : outil d'audit a11y
