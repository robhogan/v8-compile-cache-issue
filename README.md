```sh
node index.js
Hello!
```

```sh
node --require=v8-compile-cache index.js

node:internal/errors:490
    ErrorCaptureStackTrace(err);
    ^

TypeError [ERR_VM_DYNAMIC_IMPORT_CALLBACK_MISSING]: A dynamic import callback was not specified.
    at new NodeError (node:internal/errors:399:5)
    at importModuleDynamicallyCallback (node:internal/process/esm_loader:39:9)
    at Object.<anonymous> (/data/sandcastle/boxes/fbsource/xplat/js/tools/v8-compile-cache-repro/importWithEsm.js:11:1)
    at Module._compile (/data/sandcastle/boxes/fbsource/xplat/js/node_modules/v8-compile-cache/v8-compile-cache.js:192:30)
    at Module._extensions..js (node:internal/modules/cjs/loader:1308:10)
    at Module.load (node:internal/modules/cjs/loader:1117:32)
    at Module._load (node:internal/modules/cjs/loader:958:12)
    at Module.require (node:internal/modules/cjs/loader:1141:19)
    at require (node:internal/modules/cjs/helpers:110:18)
    at Object.<anonymous> (/data/sandcastle/boxes/fbsource/xplat/js/tools/v8-compile-cache-repro/index.js:11:1)
    at Module._compile (node:internal/modules/cjs/loader:1254:14)
    at Module._extensions..js (node:internal/modules/cjs/loader:1308:10)
    at Module.load (node:internal/modules/cjs/loader:1117:32)
    at Module._load (node:internal/modules/cjs/loader:958:12)
    at Function.executeUserEntryPoint [as runMain] (node:internal/modules/run_main:81:12)
    at node:internal/main/run_main_module:23:47 {
  code: 'ERR_VM_DYNAMIC_IMPORT_CALLBACK_MISSING'
}
```