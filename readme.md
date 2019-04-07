# fa-pro-netlify-test

## About

Sandbox for deploying [pro font awesome icons via npm](https://fontawesome.com/how-to-use/on-the-web/setup/using-package-managers) in production.

This is a research pivot learning sandbox venture, from static/roadblocks/headaches with another project deploying pro features via netlify.

## Working notes

[Stack Overflow question](https://stackoverflow.com/questions/55514076/npmrc-config-file-not-reading-environment-variable-to-download-private-node-mod).

Here's the [Netlify private modules gist](https://gist.github.com/biilmann/0b2250095eedc188d0c9). Netlify seems to need the .npmrc env variable syntax to include curly braces, ie, only the following works with Netlify:

1. A .npmrc file like so (the variable name doesn't matter, but syntax does)

```
@fortawesome:registry=https://npm.fontawesome.com/
//npm.fontawesome.com/:_authToken=${NPM_TOKEN}
```

2. A project-specific build environment variable configured in the project's netlify dashboard, named `NPM_TOKEN`

3. Since the .npmrc file above won't work for local development, you have to set up the font-awesome details via the [per-user configuration file](https://docs.npmjs.com/misc/config#npmrc-files) approach, via the [font-awesome global set up](https://fontawesome.com/how-to-use/on-the-web/setup/using-package-managers#installing-pro), ie:

```
npm config set "@fortawesome:registry" https://npm.fontawesome.com/ && \
npm config set "//npm.fontawesome.com/:_authToken" ABC123
```

## Solution

I pivoted from this pivot, and [came to a solution](https://github.com/brianzelip/npm-private-mods-test/commit/4fef535d0dfa73aafeb590758b1df6b34eb626bb).

There is now a .zshrc-based `$FONT_AWESOME_PRO_TOKEN`.

This allows the .npmrc file to reference it, **_using curly braces_**, which gels well with Netlify 🍻

This also means deleting project-based .env files, and loading shell env vars as discussed in the solution repo above.
