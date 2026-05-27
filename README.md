# MoonChunk Language Support

Production-ready VS Code extension for the MoonChunk language (`.mncnk`).

## Features

- Syntax highlighting for `*.mncnk` and `Moonfile`
- Extensive TextMate grammar coverage:
  - shebang
  - ANTLR-aligned control/runtime keywords (`chunk`, `export`, `moon`, `output`, `env`, `global`, `page`, `content`, `function`, loops/conditions)
  - include/import syntax (`@include`, `import ... from ...`, `as`, wildcard imports)
  - metadata keys (`metaDescription`, `ogTitle`, `twitterCard`, etc.)
  - `content { ... };` blocks with HTML tags and embedded `{expression}` highlighting
  - function declarations/calls and arrow-function signatures
  - string literals and numeric literals (`1`, `2.5`, `1f`, `2D`)
  - built-in types and booleans (`int`, `float`, `double`, `bool`, `string`, `true`, `false`, etc.)
  - lexer-aligned operators (`=>`, `==`, `!=`, `<=`, `>=`, `++`, `+`, `-`, `*`, `/`, `%`, `?`, `:`, `.`)
- Language configuration:
  - line comments (`//`)
  - bracket matching
  - auto-closing/surrounding pairs
  - indentation rules
  - folding markers (`#region` / `#endregion`)
- Snippets for common MoonChunk patterns
- In-editor Home Dashboard (`MoonChunk: Open Home Dashboard`)
- Guided walkthrough onboarding (`MoonChunk: Open Getting Started Walkthrough`)
- Post-install behavior controls via extension settings

## File Structure

- `package.json` - extension manifest and marketplace metadata
- `syntaxes/moonchunk.tmLanguage.json` - TextMate grammar
- `language-configuration.json` - editor behavior
- `snippets/moonchunk.json` - snippet definitions
- `ui/*` - dashboard webview UI
- `docs/*` - onboarding and troubleshooting docs
- `src/extension.ts` - extension entry source
- `dist/extension.js` - built entry used by VS Code
- `images/logo.png` - marketplace icon

## Dashboard & Walkthrough

- Command: `MoonChunk: Open Home Dashboard`
- Command: `MoonChunk: Open Getting Started Walkthrough`
- Command: `MoonChunk: Open Documentation Index`
- Settings:
  - `moonchunk.postInstallExperience` (`home` | `walkthrough` | `none`)
  - `moonchunk.showWalkthroughOnInstallOrUpdate`
  - `moonchunk.openDocsInEditor`

## Local Development

1. Install dependencies:

```bash
npm install
```

2. Build once:

```bash
npm run build
```

3. Run extension development host:

- Open this folder in VS Code
- Press `F5`

4. Test with sample files under `examples/`.

## Package for Marketplace

```bash
npm run package
```

The command generates a `.vsix` package.

## Publish

1. Set correct values in `package.json`:

- `publisher`
- `repository.url`
- `bugs.url`
- `homepage`

2. Login to VS Code Marketplace via `vsce` if needed.
3. Publish:

```bash
npm run publish
```

## Pre-Go-Live Checklist

- [ ] Replace placeholder org/URLs with real project values
- [ ] Bump `version` according to release strategy
- [ ] Verify icon branding in light and dark themes
- [ ] Validate highlighting with real MoonChunk codebase
- [ ] Confirm snippets and indentation behaviors
- [ ] Generate `.vsix` and install-test locally
- [ ] Publish and smoke test after install from marketplace

## License

MIT. See [LICENSE](./LICENSE).
