## nucler-parse

minimalist xml/json parser. zero deps.

```
npm i nucler-parse
```

```javascript
const { parse } = require('nucler-parse')

const data = parse('<root><item>value</item></root>')
console.log(data.root.item) // "value"
```

works with xml, json, yaml (auto-detect format).

built with [pegstr](https://pegstr.io) parser generator.

### api

`parse(input)` - returns object  
`stringify(obj)` - returns string  
`validate(input, schema)` - returns bool

### why

- other parsers too heavy (200kb+)
- this one: 8kb gzipped
- no dependencies
- supports comments in json

### known bugs

- yaml indentation sometimes wrong (use spaces not tabs)
- nested arrays >10 levels crash
- unicode emojis break in xml attributes

see [issues](https://github.com/parse-tools/nucler-parse/issues)

MIT
