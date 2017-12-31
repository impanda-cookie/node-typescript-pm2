# node-typescript-pm2
nodejs ( typescript )run with pm2

# run 
> package.json `scripts`:

```javascript
    "scripts": {
        "build": "node ./node_modules/typescript/bin/tsc  --listEmittedFiles",
        "start": "npm run build && pm2 start -x dist/app.js --no-daemon"
    }
```
# example

`docker run -d --rm --name test -v "${PWD}:/app -p 8081:80 cowpanda/node-typescript-pm2:latest"`
