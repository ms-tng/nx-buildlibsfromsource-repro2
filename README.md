# Nx `buildLibsFromSource: false` bug reproduction

Run `nx serve my-app` and observe that `my-lib` is still served from source.
When an `exports` field is added to `my-lib/package.json`, `my-lib` is correctly served from the `dist` folder.