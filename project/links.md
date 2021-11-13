# Liens utiles

[Sass releases - GitHub](https://github.com/sass/dart-sass/releases/tag/1.43.4)  
[Sass Documentation](https://sass-lang.com/documentation)  
[Sass Documentation | @import](https://sass-lang.com/documentation/at-rules/import)
[Sass Changelog](https://github.com/sass/dart-sass/blob/main/CHANGELOG.md)
[Sass - Releases](https://github.com/sass/dart-sass/releases)

>Heads up!
>The Sass team discourages the continued use of the @import rule. Sass will gradually phase it out over the next few years, and eventually remove it from the language entirely. Prefer the @use rule instead. (Note that only Dart Sass currently supports @use. Users of other implementations must use the @import rule instead.)
>What’s Wrong With @import?
>**The @import rule has a number of serious issues:**
>- @import makes all variables, mixins, and functions globally accessible. This makes it very difficult for people (or tools) to tell where anything is defined.
>- Because everything’s global, libraries must prefix to all their members to avoid naming collisions.
>- @extend rules are also global, which makes it difficult to predict which style rules will be extended.
>- Each stylesheet is executed and its CSS emitted every time it’s @imported, which increases compilation time and produces bloated output.
>- There was no way to define private members or placeholder selectors that were inaccessible to downstream stylesheets.
>The new module system and the @use rule address all these problems.