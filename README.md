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

###### Output:

Outputs come in the form of a JSON object which is the exact output of the etherscamdb check API endpoint.

For domains:
```
{ success: true, input: 'mycrypto.com', result: 'verified' }
```

```
{ success: true, input: 'idexmarket-incs.com', result: 'blocked', type: 'domain', entries: [ { id: 4286,name: 'idexmarket-incs.com',url: 'https://idexmarket-incs.com',category: 'Phishing',subcategory: 'Idex',description: 'Fake IDEX market phishing for keys',status: 'Offline' } ] }
```

For eth addresses:
```
{"success":true,"result":"blocked","type":"address","entries":[{"id":4403,"name":"freeethpromo.com","url":"http://freeethpromo.com","category":"Scamming","subcategory":"Trust-Trading","description":"Trust-Trading site","addresses":["0xcf1d62627baf1a84bed11e30cf6cdae0f1b5c296"],"ip":"185.224.137.165","nameservers":["ns3.hostinger.com","ns2.hostinger.com","ns1.hostinger.com","ns4.hostinger.com"],"status":"Active"}]}
```

For ips:
```
{"success":true,"input":"193.233.15.49","result":"blocked","type":"ip","entries":[{"id":4526,"name":"ethbig.net","url":"https://ethbig.net","category":"Scamming","subcategory":"Trust-Trading","description":"Trust trading scam site","addresses":["0xa22270850fabde01e1f5c5879ea65dd82890af31"],"ip":"193.233.15.49","nameservers":["dns2.storm-pro.net","dns1.storm-pro.net"],"status":"Offline"}]}
```
