<p align="center">
  <img src="icon/sass.svg" width="64" height="64" alt="Sass">
</p>

# Sass Extension for Zed

A [Zed](https://zed.dev) extension that adds support for the **indented Sass syntax** (`.sass` files).

This extension is purpose-built for the indentation-based `.sass` format — no braces, no semicolons.

## Features

- **Syntax highlighting** — keywords, variables, selectors, properties, functions, strings, numbers, operators, and comments all get distinct colors from your active Zed theme
- **Language server** — integrates [Some Sass Language Server](https://github.com/nicolo-ribaudo/some-sass) for autocompletion, hover info, go-to-definition, and diagnostics
- **Code outline** — navigate mixins, functions, selectors, variables, and imports via the outline panel
- **Indentation** — auto-indent after selectors, mixins, functions, control flow, and media queries
- **Bracket matching** — pairs `()`, `[]`, and `#{}` interpolation

## Installation

### From Zed Extensions (recommended)

1. Open Zed
2. Go to **Extensions** (`Cmd+Shift+X`)
3. Search for **"Sass"** and install

### Dev install (from source)

1. Clone this repository
2. In Zed, open the command palette (`Cmd+Shift+P`)
3. Run **"zed: install dev extension"**
4. Select the cloned folder

## Language Server

The extension automatically downloads and manages the [some-sass-language-server](https://www.npmjs.com/package/some-sass-language-server) via npm. No manual setup required.

If you prefer a global install:

```sh
npm i -g some-sass-language-server
```

You can configure the language server in your Zed settings:

```json
{
  "lsp": {
    "some-sass-lsp": {
      "settings": {}
    }
  }
}
```

## Grammar

Uses [bajrangCoder/tree-sitter-sass](https://github.com/bajrangCoder/tree-sitter-sass), a tree-sitter grammar specifically designed for the indented `.sass` format with an external C scanner that handles `INDENT`/`DEDENT`/`NEWLINE` tokens.

## License

[MIT](LICENSE)
