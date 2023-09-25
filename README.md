# Nx `buildLibsFromSource: false` bug reproduction

Run `nx serve my-app` and observe that `my-lib` is still served from source.

When the following is added to `my-lib/package.json`, `my-lib` is correctly served from the `dist` folder:
```
"exports": {
  ".": {
    "import": "./index.mjs"
  }
}
```

However, it should work even without an `exports` field.