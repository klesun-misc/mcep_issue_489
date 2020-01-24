For https://github.com/webpack-contrib/mini-css-extract-plugin/issues/489

Steps to reproduce `Callback was already called` in
[mini-css-extract-plugin](https://github.com/webpack-contrib/mini-css-extract-plugin) when you try to use it with
[html-webpack-plugin](https://github.com/jantimon/html-webpack-plugin) to minimize css referenced in `<link href='...'/>`  

- Clone this repo
- Run `npm ci`
- Run `node node_modules/webpack/bin/webpack.js`

Will fail with this error:
```$
Error: Callback was already called.
    at throwError (/mnt/winda/gits/mcep_issue_489/node_modules/neo-async/async.js:16:11)
    at /mnt/winda/gits/mcep_issue_489/node_modules/neo-async/async.js:2818:7
    at process._tickCallback (internal/process/next_tick.js:61:11)
```
