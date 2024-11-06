# xenpaper
Repo for [xenpaper mirror](https://luphoria.com/xenpaper)/fork.

## Building 
```
git clone https://github.com/luphoria/xenpaper
npm i
```
Temporarily add this flag to your NODE_OPTIONS env: `--openssl-legacy-provider`.
```
yarn build
```
You may need to install some global npm packages.

Build files should be in `packages/xenpaper-app/build`.  

After that you will also need to edit build/index.html, find and replace the two instances of `/static` with `./static`. Also to fix the broken icon, edit build/static/js/main.*.chunk.js, `n.p+"static/` => `"static/`. This bug happens somewhere in the build step, so I don't know how I might be able to automate this. 