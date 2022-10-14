#  Dot-Zero Tech
## Prettier Code Standard

### Node.JS
Install command: `pnpm i -D prettier`
Config: `#1`

### Svelte / Svelte-Kit
Install command: `pnpm i -D pretter prettier-plugin-svelte`
Config: `#2`

## Config #1
*.prettierrc*
```json
{
  "printWidth": 240,
  "tabWidth": 2,
  "useTabs": false,
  "semi": false,
  "singleQuote": true,
  "quoteProps": "consistent",
  "jsxSingleQuote": true,
  "trailingComma": "none",
  "bracketSpacing": true,
  "bracketSameLine": false,
  "arrowParens": "always",
  "proseWrap": "preserve",
  "htmlWhitespaceSensitivity": "strict",
  "vueIndentScriptAndStyle": true,
  "endOfLine": "lf",
  "embeddedLanguageFormatting": "auto",
  "singleAttributePerLine": false
}
```

## Config #2
```json
{
	"printWidth": 240,
	"tabWidth": 2,
	"useTabs": false,
	"semi": false,
	"singleQuote": true,
	"quoteProps": "consistent",
	"jsxSingleQuote": true,
	"trailingComma": "none",
	"bracketSpacing": true,
	"bracketSameLine": false,
	"arrowParens": "always",
	"proseWrap": "preserve",
	"htmlWhitespaceSensitivity": "strict",
	"vueIndentScriptAndStyle": true,
	"endOfLine": "lf",
	"embeddedLanguageFormatting": "auto",
	"singleAttributePerLine": false,

	"plugins": ["prettier-plugin-svelte"],
	"pluginSearchDirs": ["."],
	"overrides": [{ "files": "*.svelte", "options": { "parser": "svelte" } }]
}
```
