# svelte app

This is a project template for [Svelte](https://svelte.dev) apps. It lives at https://github.com/sveltejs/template.

To create a new project based on this template using [degit](https://github.com/Rich-Harris/degit):

```bash
npx degit sveltejs/template svelte-app
cd svelte-app
```

*Note that you will need to have [Node.js](https://nodejs.org) installed.*


## How it was build

1. Create svelte app
```js
npx degit sveltejs/template wc-svelte-clock
```
2. install the app 
```bash
cd wc-svelte-clock && yarn
```
3. Add clock in `App.svelte` taken from [clock](https://svelte.dev/repl/clock?version=3.38.2)
4. Add `customElement: true` inside rollup.config.js
5. Create `svelte:options` inside `App.svelte`
```html
<svelte:options tag=”svelte-clock” immutable={true} />
```
6. Remove unwanted code in main.js
7. To test in local add below in `public/index.html`
```html
<svelte-clock></svelte-clock>
```

## How to publish in github 

1. Create folder as docs
```bash
mkdir docs && touch docs/index.html
```
2. Bundle up 
```bash
yarn build
```
3. Copy public/build/bundle.js to docs/bundle.js

## Reference 

- https://itnext.io/svelte-web-component-5-4kb-4afe46590d99
- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site