# SeedMe Documentation

This subproject contains the AsciiDoc documentation for the SeedMe Grails plugin.

## Building Locally

To build the documentation locally:

```bash
./gradlew :seed-me-docs:asciidoctor
```

The generated HTML documentation will be available in `seed-me-docs/build/docs/`.

## Viewing the Documentation

After building, open the generated HTML file:

```bash
open seed-me-docs/build/docs/index.html
```

Or on Linux:

```bash
xdg-open seed-me-docs/build/docs/index.html
```

## Publishing to GitHub Pages

The documentation is automatically published to GitHub Pages when changes are pushed to the main branches (main, master, or grails7).

The GitHub Actions workflow (`.github/workflows/publish-docs.yml`) handles:
- Building the AsciiDoc documentation
- Publishing to GitHub Pages

### Setup GitHub Pages

To enable GitHub Pages for this repository:

1. Go to repository Settings → Pages
2. Under "Source", select "GitHub Actions"
3. The workflow will automatically deploy on the next push

## Documentation Structure

- `src/docs/asciidoc/index.adoc` - Main documentation entry point
- `src/docs/asciidoc/groovy-dsl.adoc` - Groovy DSL reference
- `src/docs/asciidoc/yaml-syntax.adoc` - YAML syntax reference
- `src/docs/asciidoc/advanced-usage.adoc` - Advanced features and patterns

## AsciiDoc Resources

- [AsciiDoc Syntax Quick Reference](https://docs.asciidoctor.org/asciidoc/latest/syntax-quick-reference/)
- [Asciidoctor Gradle Plugin](https://asciidoctor.org/docs/asciidoctor-gradle-plugin/)
