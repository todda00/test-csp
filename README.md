# Issue Reproduction for strict-csp-html-webpack-plugin

## Related Issue:
https://github.com/google/strict-csp/issues/48

This repo contains a freshly ejected CRA app with strict-csp-html-webpack-plugin added.

This reproduction examples an issue in `strict-csp-html-webpack-plugin` where the hash calculated for the inline script is incorrect when webpack builds in production. I have narrowed down the issue to using a webpack config with a filename containing [contenthash]. This fails in a fresh, ejected create-react-app as well when building in production mode. 


## Steps to Reproduce:

Clone reproduction repo
Navigate to repo root directory

Run the following:
```
npm install
npm run build
npx serve -s build
```