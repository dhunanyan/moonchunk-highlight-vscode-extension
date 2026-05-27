# Changelog

All notable changes to this project will be documented in this file.

## [1.2.0] - 2026-05-07

### Changed

- Realigned syntax highlighting rules with the current ANTLR language grammar from `moonchunk/`:
  - core control/runtime tokens (`chunk`, `export`, `moon`, `@include`, `output`, `env`, `global`, `page`, `content`, `function`, loops/conditions)
  - import/include statement highlighting
  - type and boolean token coverage
  - metadata key highlighting (`metaDescription`, `ogTitle`, `twitterCard`, etc.)
  - operator set aligned to lexer tokens (`=>`, `==`, `!=`, `<=`, `>=`, `++`, `?`, etc.)
  - `content { ... };` block support with HTML tag + `{expression}` embedded highlighting
- Updated snippets to valid current MoonChunk syntax (removed outdated `fn`/`match` style templates).
- Updated sample extension examples to modern MoonChunk syntax for easier local verification.
- Updated line-comment configuration to `//` to match lexer behavior.

## [1.1.0] - 2026-03-30

### Added

- MoonChunk Home Dashboard webview (`ui/index.html`, `ui/style.css`, `ui/script.js`)
- Walkthrough onboarding (`moonchunk.getting-started`)
- New MoonChunk commands for home/dashboard/docs/settings
- Post-install onboarding configuration options
- Documentation set under `docs/` (overview, installation, grammar, snippets, troubleshooting)
- Extended extension metadata for richer marketplace presentation

## [0.1.0] - 2026-03-26

### Added

- Initial production-ready release scaffold
- Full extension metadata for VS Code Marketplace
- Rich MoonChunk TextMate grammar
- Snippets for common language constructs
- Advanced language configuration (indentation, folding markers, auto-close rules)
- Icon assets and go-live documentation
