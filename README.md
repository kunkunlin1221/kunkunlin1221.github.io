# kunkunlin1221.github.io

Source for my personal academic homepage, live at **[https://kunkunlin1221.github.io/](https://kunkunlin1221.github.io/)**.

Built with [Jekyll](https://jekyllrb.com/) on the
[Minimal Light](https://github.com/yaoyao-liu/minimal-light) remote theme and
deployed automatically by GitHub Pages on every push to `main` (no build step
required).

## Editing the content

Most updates are data-only — edit the YAML, not the templates:

| What                                                                | Where                                         |
| ------------------------------------------------------------------- | --------------------------------------------- |
| Name, role, links, SEO, analytics                                   | `_config.yml`                               |
| About / Research Interests / News / Education / Experience / Honors | `index.md`                                  |
| Publications                                                        | `_data/publications.yml`                    |
| Projects                                                            | `_data/projects.yml`                        |
| Service (reviewing)                                                 | `_includes/services.md`                     |
| Shared publication/project row markup                               | `_includes/entry.html`                      |
| Styles                                                              | `_sass/minimal-light.scss`, `assets/css/` |
| Images / PDFs                                                       | `assets/img/`, `assets/files/`            |

Keep teaser images small (≈600 px wide) — they are displayed in a 270×123 px box.

## Running locally

```bash
bundle install
bundle exec jekyll serve   # http://localhost:4000
```

## License

The underlying theme is by Yaoyao Liu under the terms in [LICENSE](LICENSE).
