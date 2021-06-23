### I've added two scripts in the `package.json`

* `test` runs `mocha`
* `compile`compiles the `Inbox.sol`

### The issue

I can successfully run compile and it does compile(with warnings of course). But I've added in a console log in the `compile.js` file to confirm that it's compiling successfully.

But when I run the test, it gives me an error saying:

```
siddajmera@Siddharths-MacBook-Pro BuildingSmartContractsWithSolidity % npm test

> BuildingSmartContractsWithSolidity@1.0.0 test /Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity
> mocha

/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/contracts/Inbox.sol:1
pragma solidity ^0.4.17;
       ^^^^^^^^

SyntaxError: Unexpected identifier
    at wrapSafe (internal/modules/cjs/loader.js:979:16)
    at Module._compile (internal/modules/cjs/loader.js:1027:27)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at Module.require (internal/modules/cjs/loader.js:952:19)
    at require (internal/modules/cjs/helpers.js:88:18)
    at Object.<anonymous> (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/test/Inbox.test.js:5:33)
    at Module._compile (internal/modules/cjs/loader.js:1063:30)
    at Object.Module._extensions..js (internal/modules/cjs/loader.js:1092:10)
    at Module.load (internal/modules/cjs/loader.js:928:32)
    at Function.Module._load (internal/modules/cjs/loader.js:769:14)
    at ModuleWrap.<anonymous> (internal/modules/esm/translators.js:199:29)
    at ModuleJob.run (internal/modules/esm/module_job.js:152:23)
    at Loader.import (internal/modules/esm/loader.js:166:24)
    at formattedImport (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/node_modules/mocha/lib/esm-utils.js:7:14)
    at Object.exports.requireOrImport (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/node_modules/mocha/lib/esm-utils.js:48:32)
    at Object.exports.loadFilesAsync (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/node_modules/mocha/lib/esm-utils.js:73:20)
    at singleRun (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/node_modules/mocha/lib/cli/run-helpers.js:125:3)
    at Object.exports.handler (/Users/siddajmera/Desktop/development/Ethereum/BuildingSmartContractsWithSolidity/node_modules/mocha/lib/cli/run.js:366:5)
npm ERR! Test failed.  See above for more details.

siddajmera@Siddharths-MacBook-Pro BuildingSmartContractsWithSolidity %
```