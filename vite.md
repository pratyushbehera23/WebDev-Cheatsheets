# Vite

We need build tools while making big application mostly using a framework/library

vitejs.dev
Vite - a tool

dev server
module bundler

Vite vs Traditional Module Bundlers (like WebPack):
WebPack - bundles all your JS modules, CSS and other assets every time you make a change (this can get really slow as your app grows)
Vite - Vite takes advantage of native ES Modules. Serves directly to the browser. Uses Rollup to bundle files for production (npm run build)

> npm create vite@latest my-app-name

Select a framework:
    Vanilla Vue React Preact Lit Svelte Others

Select a variant:
    JS TS JS+SWC TS+SWC

```sh
> cd my-app-name
> npm install / npm i
> npm run dev

# for production:
> npm run build
# preview the build:
> npm run preview
```
