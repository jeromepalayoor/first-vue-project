# first-vue-project

This is my first Vue.js 3 project that I built by following [a tutorial series](https://www.youtube.com/playlist?list=PL4cUxeGkcC9hYYGbV60Vq3IXYNfDk8At1).
See the site [here](https://jeromepalayoor.github.io/first-vue-project/)

## Project setup
```
npm install
```

### Compiles and hot-reloads for development
```
npm run serve
```

### Compiles and minifies for production
```
npm run build
```

### How to deploy to github pages

```
npm i gh-pages --save-dev
```

Make sure to have these stuff in package.json file:

```
    "homepage": "https://<username>.github.io/<project-name>",
    "scripts": {
        ...,
        ...,
        "deploy": "gh-pages -d dist"
    },
```

Make sure to have these stuff in vue.config.js file:

```
const { defineConfig ...
module.exports = defineConfig({
  transpileDependencies: true,
  publicPath: process.env.NODE_ENV === 'production' ? '/<project-name>/' : '/',   #IMPORTANT
})

```