# Consulta IoC's

```
$ npm install
```
## Running in Docker:

Build the container:

```bash
docker build -t puppeteer-chrome-linux .
```

Run the container by passing `node -e "<index.js content as a string>"` as the command:

```bash
 docker run -i --init --rm --cap-add=SYS_ADMIN \
   --name puppeteer-chrome puppeteer-chrome-linux \
   node -e "`cat index.js`"
```

There's a full example at https://github.com/ebidel/try-puppeteer that shows
how to run this Dockerfile from a webserver running on App Engine Flex (Node).