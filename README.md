# Markdeep Rasterizer

This module can be used to convert [Markdeep](https://casual-effects.com/markdeep/) files
to static HTML. Converting Markdeep files to static HTML greatly improves load times in complex documents. It can also be beneficial to users who choose to disable JavaScript (the generated document still needs JavaScript to render equations though). The conversion is performed using Chromium via [Puppeteer](https://github.com/puppeteer/puppeteer).

This conversion can also be attempted using Firefox of Chrome in headless mode from the command line, but the generated result still attempts to execute Markdeep.

# Example

Here is an example of a complex Markdeep document before and after conversion to static HTML:

- [Source Markdeep](https://google.github.io/filament/Filament.md.html)
- [Rasterized Markdeep](https://google.github.io/filament/Filament.html)

# Usage

This module is meant to be executed directly with `npx`:

```bash
npx markdeep-rasterizer <file1> <file2> ... <fileN> <outDirectory>
```

Where each `<fileX>` is a path to a Markdeep file ending in `.md.html`. The output `.html` files
will be generated in the specified output directory.

Here is a real-world example from [Filament](https://github.com/google/filament):

```bash
npx markdeep-rasterizer ../../docs/Filament.md.html ../../docs/Materials.md.html  ../../docs/
```

# License

Apache License
Version 2.0, January 2004
