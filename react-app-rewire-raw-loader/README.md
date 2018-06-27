# react-app-rewire-inline-source

Enable source code inlining capabilities in a [react-app-rewired](https://github.com/timarney/react-app-rewired) application.

Adds the ability to import files as a string.

Add to config overrides:

```
/* config-overrides.js */
const rewireRawLoader = require('@baristalabs/react-app-rewire-raw-loader')

module.exports = function override (config, env) {
    config = rewireRawLoader(config, env)
    return config
}
```

Then:

```
 const data = require('raw-loader!./myFile.js') as string;
 console.dir(data);
 ```