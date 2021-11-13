# Sass workshop

## <a id="index">Index</a>

[1 - Sass vs CSS](#1)
[2 - Pattern 7-1](#2)
[3 - Règles d'import](#3)
[Liens  utiles](#links)

## <a id="1">1 - Sass vs CSS</a>

CSS et Sass : Sass ne permet pas de faire plus que ce que vous pouvez déjà faire en CSS.  
Le fichier de style que vous allez générer à la fin et qui sera lu par le navigateur est en CSS.  
Sass apporte des fonctionnalités très utiles pour : gagner du temps, avoir une meilleure organisation de vos règles de style.  
Si vous connaissez CSS, vous savez déjà utiliser Sass !  

Quelques avantages de Sass :

- Répartir vos règles dans des fichiers distincts (partials)
- Eviter de répéter plusieurs fois les mêmes règles (mixins, nesting)
- Intégrer vos media queries dans vos composants (c'est déjà possible en CSS mais moins lisible)
- Tout compiler en un seul fichier CSS "classique" (on peut aussi générer plusieurs fichiers si besoin)

___

## <a id="2">2- Pattern 7-1</a>

<pre>
sass/
|
|– abstracts/
|   |– _variables.scss    # Sass Variables
|   |– _functions.scss    # Sass Functions
|   |– _mixins.scss       # Sass Mixins
|   |– _placeholders.scss # Sass Placeholders
|
|– base/
|   |– _reset.scss        # Reset/normalize
|   |– _typography.scss   # Typography rules
|   …                     # Etc.
|
|– components/
|   |– _buttons.scss      # Buttons
|   |– _carousel.scss     # Carousel
|   |– _cover.scss        # Cover
|   |– _dropdown.scss     # Dropdown
|   …                     # Etc.
|
|– layout/
|   |– _navigation.scss   # Navigation
|   |– _grid.scss         # Grid system
|   |– _header.scss       # Header
|   |– _footer.scss       # Footer
|   |– _sidebar.scss      # Sidebar
|   |– _forms.scss        # Forms
|   …                     # Etc.
|
|– pages/
|   |– _home.scss         # Home specific styles
|   |– _contact.scss      # Contact specific styles
|   …                     # Etc.
|
|– themes/
|   |– _theme.scss        # Default theme
|   |– _admin.scss        # Admin theme
|   …                     # Etc.
|
|– vendors/
|   |– _bootstrap.scss    # Bootstrap
|   |– _jquery-ui.scss    # jQuery UI
|   …                     # Etc.
|
`– main.scss              # Main Sass file
</pre>

[:top: Retour à l'index](#index)
___

## <a id="3">3 - Règles d'import</a>

Avertissement sur le site officiel sass-lang.[^1]

Heads up!
The Sass team discourages the continued use of the @import rule. Sass will gradually phase it out over the next few years, and **eventually remove it from the language entirely**. Prefer the @use rule instead. (Note that **only Dart Sass currently supports @use**. Users of other implementations must use the @import rule instead.)
What’s Wrong With @import?
The @import rule has a number of serious issues:

- **@import makes all variables, mixins, and functions globally accessible**. This makes it very difficult for people (or tools) to tell where anything is defined.
- Because everything’s global, libraries must prefix to all their members to avoid naming collisions.
- @extend rules are also global, which makes it difficult to predict which style rules will be extended.
- Each stylesheet is executed and its CSS emitted every time it’s @imported, which increases compilation time and produces bloated output.
- There was **no way to define private members** or placeholder selectors that were inaccessible to downstream stylesheets.
The new module system and the @use rule address all these problems.

___

## <a id="links">Liens</a>

### Général

[Sass Download - GitHub](https://github.com/sass/dart-sass/releases/tag/1.43.4)  
[Sass Documentation](https://sass-lang.com/documentation)  
[Sass Changelog](https://github.com/sass/dart-sass/blob/main/CHANGELOG.md)  
[Sass - Releases](https://github.com/sass/dart-sass/releases)

### Motif 7-1

[OpenClassrooms](https://openclassrooms.com/fr/courses/6106181-simplifiez-vous-le-css-avec-sass/6599201-utilisez-le-systeme-7-1-pour-une-codebase-plus-simple-a-gerer)  
[Sass Guidelines](https://sass-guidelin.es/fr/#architecture)

[^1]:[Avertissement Sass | @import](https://sass-lang.com/documentation/at-rules/import)  

### Youtube

[Kevin Powell - @use/@forward](https://www.youtube.com/watch?v=CR-a8upNjJ0)

### Autres ressources

[normalize.css](https://necolas.github.io/normalize.css/8.0.1/normalize.css)
[minireset.css](https://jgthms.com/minireset.css/)

[:top: Retour à l'index](#index)