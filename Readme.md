

## Multilanguage support (en/de)

To use multi language support, I make use of [quarto profiles](https://quarto.org/docs/projects/profiles.html). 

1. We create two profiles: `en` / `de`
2. Each has its own YAML file: `_quarto-en.yml` and `quarto-de.yml` and `output-dir` (`_site/en` and `_site/de`)
3. We specify a default profile using [groups](https://quarto.org/docs/projects/profiles.html#profile-groups)
4. We conditionally show content using divs with the `.content-visible when-profile="en"` syntax
5. To Render, you must specify a profile (e.g. `--profile en`) ~~and also use the option `--no-clean`~~
6. To publish, you cannot use `quarto publish` anymore, since this is `output-dir`-aware. Rather, use netlify with the 
7. In the root dir, specify a `_redirects` to direct users to one of the subsites (since the root is empty)
