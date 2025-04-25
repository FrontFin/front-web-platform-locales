# Localization files for the front-web-platform repository

Translation is managed by the third party tool Crowdin. When new strings are automatically translated by the AI or changed by the proofreaders Crowdin pushes changes to the `l18n_main` branch and creates the pull request. Developers needs to verify that all the translated strings are good and merge the PR.

## Typical errors:

1. Missing/incorrect tag. For example in `en/catalog.json` we have:

```json
{
  "body": "Some <1>important</1> string."
}
```

but in the `es/catalog.json` we've got it without closing tag:

```json
{
  "body": "Alguna cadena <1>importante."
}
```

2. Incorrect placeholder. For example in `en/catalog.json` we have:

```json
{
  "body": "Some {{one}} {{two}} string."
}
```

but in the `es/catalog.json` we've got it wrapped without only one bracket or with incorrect/translated name:

```json
{
  "body": "Algunas {one} {{dos}} cuerdas."
}
```
