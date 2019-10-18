# ssp-typescript-snippets

---

This extension contains code snippets for React with Typescript. It is a fork of https://github.com/sw-yx/swyx-react-typescript-snippets made by swyx. Improved by automatically adding the folder name as CamelCase, and moving the interface below the component.

It contains just two snippets: `rfc` for a stateless functional component, and `imr` to import React because that tends to happen a lot.

## Installation

Go to the extensions panel and search for 'ssp-typescript-snippets'.

## Supported languages (file extensions)

- TypeScript (.ts)
- TypeScript React (.tsx)

## Snippets

Below is a list of all available snippets and the triggers of each one. The **⇥** means the `TAB` key.

| Trigger | Content                                        |
| ------: | ---------------------------------------------- |
|  `rfc→` | `create a react function component (no hooks)` |
|  `imr→` | `import react`                                 |

```json
{
	"import react": {
		"prefix": "imr",
		"body": ["import React from 'react'"],
		"description": "import react"
	},
	"React Function Component": {
		"prefix": "rfc",
		"body": [
			"import React from 'react';",
			"",
			"export const ${TM_DIRECTORY/^.+\\/(.*)$/${1:/pascalcase}/g}$1: React.FC<${TM_DIRECTORY/^.+\\/(.*)$/${1:/pascalcase}/g}$1Props> = function ({ $2 }) {",
			"  return (",
			"    $0",
			"  );",
			"};",
			"",
			"type ${TM_DIRECTORY/^.+\\/(.*)$/${1:/pascalcase}/g}$1Props = { $2: $3 }",
			""
		],
		"description": "Create a React Function Component"
	}
}
```

## Publishing

`vsce package`

## License

MIT
