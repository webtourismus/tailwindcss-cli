# Use Tailwind CSS without Node.js

This is a patched version of the standalone CLI build of Tailwind CSS for Linux x64 systems, easily installable as a composer package.
Contrary to the default CLI, this patched version includes also postcss-import and postcss-nested bundled inside the CLI executable.

1. Install with `composer require webtourismus/tailwindcss-cli`
2. Execute with `./vendor/bin/tailwindcss`
3. (optional) If you want to use import and/or nesting in your CSS source file, use the `--postcss` parameter to specify your PostCSS config file.

Usage example:
```
./vendor/bin/tailwindcss --input my_tailwind_source.css --output my_compiled_tailwind.css --content my_site/*.html --postcss my_custom_postcss.config.css
```

Example `postcss.config.js` file with import and nesting enabled:
```
module.exports = {
  plugins: {
    'postcss-import': {},
    'tailwindcss/nesting': {},
     tailwindcss: {},
     autoprefixer: {},
  }
}
```


See [tailwindcss.com/blog/standalone-cli](https://tailwindcss.com/blog/standalone-cli) for more instructions.  
See [tailwindcss.com/docs/using-with-preprocessors](https://tailwindcss.com/docs/using-with-preprocessors#nesting) for PostCSS options.
