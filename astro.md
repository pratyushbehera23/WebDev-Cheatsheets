# Astro

Astro - mainly a static site generator
UI agnostic - can use any framework (react,vue,angular,svelte,..)
Good for building: Docs-site, blogs, portfolio/marketing/landing-page,

```sh
npm create astro@latest
# downloads astro binary stuff & asks: projectName, gitrepo, TS, ...
npm dev
# localhost:3000
```

## .astro file

```astro
---
// node.js
---

<Layout>
    <!-- html -->
</Layout>

<Style>
    <!-- /* css */ -->
</Style>

<Script>
    <!-- // js -->
</Script>
```
