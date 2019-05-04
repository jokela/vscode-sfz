# vscode-sfz README

Provides [SFZ format](https://sfzformat.com/) support for [Visual Studio Code](https://code.visualstudio.com/).

## Features

1. Syntax highlighting for SFZ headers, opcodes, and settings
2. A theme based on Dark+ that differentiates between different opcode types
3. Parameter validation for most documented opcodes
4. Snippets

## Known Issues

Like everybody else, I haven't fully dealt with the myriad ways that modulation destinations can be combined. The logic seems capturable with regular expressions, but enumerating the validations (i.e. which opcode combinations result in which units/ranges) will take time.

## Release Notes

### 0.0.1
- Initial version with syntax highlighting, parameter validation, and header snippets.
