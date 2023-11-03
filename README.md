# riemannzeta5.github.io

This repo hosts sites for my non-WordPress content. This would include for example games (dynamic / JavaScript apps), media files like textbooks, and so on.

Right now, it hosts just my textbooks site.

## Pointers

My published website content is in the `gh-pages` branch. One of the things I noticed is that if I have a file structure like:

```yaml
- title_a
    - index
    - title_b
```

Then the link `title_a/title_b` would work, but `title_a/title_b/` (with the trailing `/`) wouldn't work. This is because the trailing `/` would indicate that `title_b` should be a folder, like:

```yaml
- title_a
    - index
    - title_b
        - index
```

In order to avoid frustrations with one-character mistypes, I'm going to structure all my content to be in `index` files, where what previously could be the name of the file will instead be the parent folder. This makes my URL paths more manageable for users, since GitHub Pages automatically accepts both `title_a/title_b/` and `title_a/title_b` (with or without trailing `/`) in the latter case.
