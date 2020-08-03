I'm going to try and learn ReactJS and build out [my blog](https://neutrollized.github.io/react-blog) as I go along

## How to Deploy ReactJS app into your GitHub Pages
### 1 - [Create your GitHub Pages site](https://docs.github.com/en/github/working-with-github-pages)

### 2 - [Create new ReactJS app](https://reactjs.org/docs/create-a-new-react-app.html) in a new repo
- your **React app name** will also be the repo name as well as the path in your URL: `https://USERNAME.github.io/REPO`

### 3 - Install gh-pages
- change to your React app directory
- `npm install gh-pages --save-dev`
- edit `package.json` to add:

```
"homepage": "http://neutrollized.github.com/react-blog",
```

and 

```
"scripts": {
    "predeploy": "npm run build",
    "deploy": "gh-pages -d build",
    ...
}
```

### 4 - Build & deploy it
`npm run deploy` should give you an output similar to:
```
> react-blog@0.1.0 predeploy /Users/glenyu/github/react-blog
> npm run build


> react-blog@0.1.0 build /Users/glenyu/github/react-blog
> react-scripts build

Creating an optimized production build...
Compiled successfully.

File sizes after gzip:

  39.39 KB  build/static/js/2.0d7d43cd.chunk.js
  780 B     build/static/js/runtime-main.796b35e1.js
  647 B     build/static/js/main.492cd51b.chunk.js
  547 B     build/static/css/main.5f361e03.chunk.css

The project was built assuming it is hosted at /react-blog/.
You can control this with the homepage field in your package.json.

The build folder is ready to be deployed.

Find out more about deployment here:

  bit.ly/CRA-deploy


> react-blog@0.1.0 deploy /Users/glenyu/github/react-blog
> gh-pages -d build

Published
```
