# elm-benchmark-helper

Bootstraps [BrianHicks/elm-benchmark][eb] in your project.

[eb]: https://github.com/BrianHicks/elm-benchmark

This project is [merged][pr] to [elm-benchmark][eb] upstream.
When other features are ready, this will be released as part of the official elm-benchmark CLI!

[pr]: https://github.com/BrianHicks/elm-benchmark/pull/40

For the mean time, you can install and use it as described below.

# Install

```sh
$ npm install ymtszw/elm-benchmark-helper -D
```

Not published to `npm` registry.

You may install globally (with `-g` option) if you want to.

# Usage

```sh
$ node_modules/.bin/elm-benchmark init    # Generates benchmarks/ directory with sample benchmark app
$ node_modules/.bin/elm-benchmark compile # Default output file is docs/index.html
$ open docs/index.html

$ node_modules/.bin/elm-benchmark install # Just installs Elm packages in benchmarks/elm-package.json
```

Re-running `init` will not overwrite existing `benchmarks/elm-package.json` and `benchmarks/Benchmarks.elm`.

Uses `node_modules/.bin/elm-*` binaries if they exist, otherwise look for globally installed Elm binaries.

# Directory Structure

```
(Your Elm project directory)
|- elm-package.json # Required
|- elm-stuff/
|- src/
|- docs/
|  \- index.html # Default compile target of benchmark app
\- benchmarks/
   |- elm-package.json # Generated. Will have ['../src', '.'] as `source-directories`
   |- Benchmarks.json  # Generated
   \- elm-stuff/
```
