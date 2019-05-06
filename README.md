# vscode-sfz README

Provides [SFZ format](https://sfzformat.com/) support for [Visual Studio Code](https://code.visualstudio.com/).

![Screenshot](images/screenshot01.png)

## Features

1. Syntax highlighting for SFZ headers, opcodes, and settings
2. A theme ("Dark+ for SFZ") based on Dark+ for coloring SFZ-specific features
3. Parameter validation for most documented opcodes
4. Some snippets for creating and editing SFZ files

## Editing

- Syntax highlighting and parameter validation are handled by a set of [TextMate Language Grammars](https://macromates.com/manual/en/language_grammars) found in the *syntaxes/sfz.tmLanguage.json* file.
    - Opcode token definitions are organized by SFZ version ([v1](https://sfzformat.com/opcodes/sfz1), [v2](http://sfzformat.com/opcodes/sfz2), [ARIA](https://sfzformat.com/opcodes/aria)) and [category](https://sfzformat.com/opcodes/categories) (e.g. Sound Source or Region Logic). To disable a group of patterns (e.g. ARIA-specific instrument setting opcodes), delete the corresponding #include line at the top of the tmLanguage file.
    - Parameter validations are organized by type (float, int, string) and range (for example, validation of floats between 0 and 100 is in the "float_0-100" object).
- Color assignments can be changed in the *themes/sfz.theme.json* file. For a guide, I used Simon Cann's [SFZTools for UltraEdit](https://noisesculpture.com/sfz-tools/). Tokens defined specifically for this theme are at the top of the file.
- Snippets can be changed in the *snippets/sfz.json* file.

## Resources

- [The SFZ Format](https://sfzformat.com/)
- [Visual Studio Code Language Extensions](https://code.visualstudio.com/api/language-extensions/overview)
- [Visual Studio Code Themes](https://code.visualstudio.com/api/extension-guides/color-theme)

## Known Issues

- Many modulation parameters are only evaluated as to whether they are numbers, rather than against valid ranges.
- Floats in scientific notation are not treated as valid.
- The effects "type" opcode is not validated as I can't find any documentation on it.
- #define substitutions are currently highlighted as invalid.

## Release Notes

### 0.0.2 2019-05-05
- Added more modulation destinations.
### 0.0.1 2019-05-03
- Initial version with syntax highlighting, parameter validation, and header snippets.
