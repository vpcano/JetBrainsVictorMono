# JetBrainsVictor Mono font

This font is a combination of the [JetBrainsMono](https://www.jetbrains.com/lp/mono/) font and the [Victor Mono](https://github.com/rubjo/victor-mono) font for italic and bold italic families, trying to mimic the [Operator Mono](https://www.typography.com/fonts/operator/overview) font for free.


## How to use

1. CLone the repo and install all `*.ttf` files from the `ttf` folder in your OS.
2. Enable the font and font ligatures in your editor of choice. For VSCode:
```js
"editor.fontFamily": "'JetBrainsVictorMono'",
"editor.fontLigatures": true,
```
3. Enable italic font on the keywords of your choice. See [scope naming](https://www.sublimetext.com/docs/scope_naming.html). For example, on VSCode:
```js
"editor.tokenColorCustomizations": {
    "textMateRules": [
        {
            "scope": [
                "comment",
                "storage.modifier", //static keyword
                "storage.type.class",
                "storage.type.class.js", //class keyword
                "entity.name.type.class", //class names
                "entity.other.attribute-name",
                "entity.other.attribute-name.html",
                "entity.other.attribute-name.tag.jade",
                "entity.other.attribute-name.tag.pug",
                "markup.italic",
                "keyword", //import, export, return…
                "keyword.control",
                "variable.language",
                "constant", //String, Number, Boolean…, this, super
            ],
            "settings": {
                "fontStyle": "italic",
            }
        },
        {
            "scope": ["strong", "markup.bold", "markup.heading"],
            "settings": {
                "fontStyle": "bold"
            }
        },
        {
            "scope": ["markup.underline"],
            "settings": {
                "fontStyle": "underline"
            }
        },
        {
            "scope": [
                "invalid",
                "keyword.operator",
                "constant.numeric",
                "entity.other.attribute-name"
            ],
            "settings": {
                "fontStyle": ""
            }
        }
    ]
},
```

## References

Inspired by font [Hactor](https://github.com/dqisme/Hactor) (combination of Hack and Victor Mono) by [dqisme](https://github.com/dqisme).

- [Operator Mono](https://www.typography.com/fonts/operator/overview)
- [Victor Mono](https://github.com/rubjo/victor-mono)
- [https://gist.github.com/junagao/f785ed77589246a3d063273b3a56f114](https://gist.github.com/junagao/f785ed77589246a3d063273b3a56f114)
