# esdb-check
npm package to wrap the check endpoint for etherscamdb.info REST api

Created by [blurpesec](https://twitter.com/blurpesec) of [MyCrypto](https://mycrypto.com)

###### To add:

```
npm install esdb-check
```

###### Example run:

```
  const check = require('esdb-check');
  const esdbcheck = new check();
  
  esdbcheck.check('mycrypto.com').then(function(output) {
    console.log(output);
  })
  ```
