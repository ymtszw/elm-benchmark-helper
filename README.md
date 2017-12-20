# elm-benchmark-helper

Bootstraps [BrianHicks/elm-benchmark][eb] in your project.

[eb]: https://github.com/BrianHicks/elm-benchmarks

# Install

```sh
$ npm install elm-benchmark -D
```

You may install globally (with `-g` option) if you want to.

# Usage

```sh
$ node_modules/.bin/elm-benchmark init
$ node_modules/.bin/elm-benchmark compile
$ open docs/index.html

$ node_modules/.bin/elm-benchmark install # Just installs Elm packages in benchmarks/elm-package.json
```

`init` generates `benchmarks/` directory with sample benchmark application.
Re-running `init` will not overwrite existing `benchmarks/elm-package.json` and `benchmarks/Benchmarks.elm`.

# Directory Structure

```
(Your Elm project directory)
|- elm-package.json # Required
\- benchmarks/
   |- elm-package.json # Generated
   \- Benchmarks.json  # Generated
```
