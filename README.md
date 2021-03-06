# co2certificate-validator
**Validation Module for automated co2 offset certificate validation**

[![CO2Offset](https://api.corrently.io/v2.0/ghgmanage/statusimg?host=co2certificate-validator&svg=1)](https://co2offset.io/badge.html?host=co2certificate-validator)


Use this to digitaly validate co2 certificates as you might get programmatically via services like [CO2Offset on RapidAPI](https://rapidapi.com/stromdao-stromdao-default/api/co2-offset).

## Installation
```shell
npm install --save co2certificate-validator
```

## Usage
```javascript
const Validator = require("co2certificate-validator");
const certificate = '0x971032fdCD88E71A880b539DEc415D1e48441DAF';
const app = async function() {
	let instance = new Validator();
  const validationResult = await instance.validation(certificate);
	console.log('Is Valid?', validationResult);
}
app();
```


## Sample certificate
```Javascript
{
  compensation: "0x971032fdCD88E71A880b539DEc415D1e48441DAF",
  certificate: {
    tree: "0x15b6F57D958A86afA4B3EB8C74949c3171A43B63",
    issueDate: 1628467200000,
    issuer: "Plant-My-Tree",
    issuersId: "1007-220616",
    lifeTime: 60549120000000,
    lifeTimeCO2: 1000000,
    meta: "25582 Hohenaspe",
    trees: 1,
    updated: 1629757247817,
    treecompensation: {
      actualSincePlanted: 24,
      availLifetime: 978283,
      usedLifetime: 21717,
      cnt: 3,
      nonce: "0x8bfF8E183F0f627cd994Dbc9119aB607E1140b51"
      }
  },
  co2: 20001,
  co2requested: 20001,
  meta: {
    co2: 20001,
    tree: "0x15b6F57D958A86afA4B3EB8C74949c3171A43B63"
  },
  nonce: "0x8bfF8E183F0f627cd994Dbc9119aB607E1140b51",
  seq: 3,
  signature: "0x7871b74f0d2169a6c0d0a32c06db7401261d6428822ef00d80e1cd0a264e80ee6d56b792616b7ca8b56e5f1ed51148d767a870c831aad9790d4a25785f69dbd41c",
  timeStamp: 1629935057909,
  tree: "0x15b6F57D958A86afA4B3EB8C74949c3171A43B63",
  owner: "0x2B5672fEfF4F923104cdBDc59afAAb864E5C2179",
  cleared: true
}
```
