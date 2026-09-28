# Nouvelles fonctionnalités HTML et CSS

Recherchez des informations sur les nouvelles fonctionnalités suivantes :

## HTML

- `API Popover`
  L'attribut popover transforme n'importe quel élément en calque top-layer géré nativement (fermeture au clic extérieur, focus, Échap), avec ::backdrop pour le fond assombri.

## CSS

### Positionnement et mise en page

- `Anchor Positioning`
  Attache un élément à un autre sans JavaScript de calcul de position : anchor-name nomme la cible, anchor() lit ses bords depuis l'élément positionné.

- `CSS Masonry` (Firefox)
  grid-template-rows: masonry empile les éléments d'une grille en comblant les vides, façon Pinterest — sans bibliothèque JS de calcul de disposition.

- `Container Queries`
  Les media queries deviennent contextuelles : elles s'appliquent à la taille du conteneur parent, pas à la fenêtre. Cela permet de créer des composants réactifs indépendants de la taille de l'écran.

### Animations et transitions

- `calc-size() & interpolate-size`
  Rend enfin possible l'animation vers auto : plus besoin de mesurer la hauteur en JavaScript avant de lancer une transition d'accordéon.

- `@starting-style`
  Définit l'état de départ d'une transition lorsqu'un élément apparaît (passe de display: none à visible) — l'effet d'entrée en fondu qui nécessitait du JavaScript devient une simple transition CSS.

- `@property`
  Déclarer le type d'une variable CSS personnalisée la rend animable en douceur. Ici, un <angle> anime un dégradé conique sans JavaScript.

- `animation-timeline: view()`
  Lie une animation à la position de scroll, sans écouteur JavaScript. Faites défiler le cadre ci-contre.

### Valeurs et couleurs

- `attr() typé`
  L'ancienne attr() ne renvoyait que du texte. La nouvelle version accepte un type explicite (<color>, <length>…), utilisable dans des propriétés comme background-color.

- `Syntaxe de couleur relative`
  Dérive une couleur à partir d'une autre en modifiant un seul canal — ici, quatre teintes calculées depuis une seule couleur de base, sans variables dupliquées.

## Vérification de compatibilité

Testez chaque fonctionnalité dans les versions récentes de Chrome et de Firefox. Pour chacune, indiquez les navigateurs et versions qui la prennent en charge, en vous appuyant sur, CanIUse, MDN Web Docs (section « Browser compatibility ») ou une autre source fiable. Distinguez la prise en charge activée par défaut de celle qui nécessite une option expérimentale.

Si une fonctionnalité n'est pas activée par défaut, vérifiez d'abord la procédure correspondant à la version du navigateur utilisée : les options expérimentales et leurs noms peuvent changer.

- **Chrome** : ouvrez `chrome://flags`, recherchez le nom de la fonctionnalité ou de l'option indiquée par une source fiable, sélectionnez **Enabled** si elle existe, puis cliquez sur **Relaunch**. Pour revenir au réglage initial, choisissez **Default**.
- **Firefox** : ouvrez `about:config`, confirmez l'avertissement, recherchez le nom exact de la préférence expérimentale indiqué par une source fiable et modifiez-la selon les instructions de cette source. Redémarrez Firefox si nécessaire. Pour annuler, réinitialisez la préférence.

Pour chacune des fonctionnalités, créez un petit exemple de code HTML/CSS qui illustre son utilisation. Vous pouvez utiliser des ressources en ligne comme MDN Web Docs, Web.dev, Alsacreations, CSS-Tricks ou les spécifications officielles pour trouver des informations détaillées.
