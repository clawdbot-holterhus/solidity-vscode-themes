# Solidity VS Code Color Themes

5 carefully crafted color themes for VS Code / code-server, designed specifically for **Solidity smart contract development and auditing**.

Each theme includes **47 Solidity-specific token rules** covering all the granular scopes from the Solidity Visual Auditor extension (visibility modifiers, state mutability, assembly blocks, security-sensitive transaction variables, NatSpec documentation, and more), plus **50-70 general-purpose rules** for a complete editing experience.

## Themes

### Dark Themes

| Theme | Description |
|-------|-------------|
| **Solidity Catppuccin Mocha** | Rich pastels on a cozy dark background. The flagship Catppuccin flavor — warm, vibrant, and easy on the eyes during long audit sessions. |
| **Solidity Nord** | Muted arctic blues and greens. Clean, minimal, and distraction-free. Based on the Nord color palette. |
| **Solidity Tokyo Night** | Modern purple and blue accents on a deep navy background. Inspired by Tokyo's city lights at night. |

### Light Themes

| Theme | Description |
|-------|-------------|
| **Solidity Catppuccin Latte** | Warm cream pastels on an off-white background. The lightest Catppuccin flavor — gentle on the eyes without washing out. |
| **Solidity GitHub Light** | Clean and professional. Follows GitHub's proven light theme conventions — familiar and readable. |

## Color Mapping Philosophy

Each theme maps Solidity syntax elements to colors with semantic consistency:

| Element | Role | Visual Treatment |
|---------|------|------------------|
| **Keywords** (`function`, `if`, `return`) | Control flow & declarations | Strong accent color |
| **Types** (`contract`, `struct`, `interface`, `enum`) | Type definitions | Italic, warm/distinct hue |
| **Functions** | Callable names | Clear blue-family |
| **Variables** | Data references | Neutral/subtle |
| **Strings** | Literal values | Green-family |
| **Numbers/Constants** | Literal values | Warm accent |
| **Comments** | Documentation | Muted/gray, italic |
| **Storage Modifiers** (`memory`, `storage`, `calldata`) | Data location | Teal/cyan, underlined |
| **Visibility** (`public`, `private`, `external`) | Access control | Underlined; `external` in warning color |
| **Events** | Log emissions | Distinct from types (pink/purple) |
| **Assembly/Unchecked** | Low-level/risky blocks | Bold + underline in warning color |
| **Security-sensitive** (`msg.sender`, `tx.origin`) | Audit-critical | Bold + underline in red/warning |
| **NatSpec** (`@param`, `@return`, etc.) | Documentation tags | Muted, unobtrusive |

## Installation

### For code-server

Already installed if you're reading this from the extensions directory. Just select a theme:

1. Open Command Palette (`Ctrl+Shift+P`)
2. Type "Color Theme"
3. Select any theme prefixed with "Solidity"

### For VS Code

Copy the entire `solidity-themes-custom` directory to your VS Code extensions folder:

```bash
# Linux/macOS
cp -r solidity-themes-custom ~/.vscode/extensions/

# Windows
xcopy /E solidity-themes-custom %USERPROFILE%\.vscode\extensions\solidity-themes-custom
```

Then reload VS Code and select a theme from `Preferences > Color Theme`.

## Requirements

For full Solidity syntax highlighting with all 47 Solidity-specific rules, install the **Solidity Visual Auditor** extension (`tintinweb.solidity-visual-auditor`), which provides the granular TextMate scopes these themes target.

Without it, the general-purpose rules still work great for standard Solidity highlighting.

## Palette Sources

All colors are sourced from official palette definitions:

- **Catppuccin**: [catppuccin/palette](https://github.com/catppuccin/palette) v1.7.1
- **Nord**: [nordtheme.com](https://www.nordtheme.com/docs/colors-and-palettes) (nord0–nord15)
- **Tokyo Night**: [enkia/tokyo-night-vscode-theme](https://github.com/enkia/tokyo-night-vscode-theme)
- **GitHub Light**: [primer/github-vscode-theme](https://github.com/primer/github-vscode-theme)

## License

MIT
