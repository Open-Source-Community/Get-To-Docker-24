
## A

### alpine-gcc


```Dockerfile
FROM alpine

RUN apk add g++
```



---

### alpine-hello-world

```Dockerfile
FROM alpine-gcc

COPY main.cpp /usr/hello-world/

WORKDIR /usr/hello-world

RUN g++ -o Main main.cpp

CMD ["./Main"]
```


---

## B


```Dockerfile
FROM node:19-alpine

COPY package*.json /app/
COPY src /app/

WORKDIR /app

RUN npm install

CMD ["node", "app.js"]
```


#### Errors are:

1) `FROM` instruction should be first and the `image` should have `npm` in it so we use `node:19-alpine`.

2) In the `COPY` instructon, the folder we are copying to might not be there so we need to add `/` after the folder name to create i if it's not present.

3) The last line, `node app.js` is what we want to run when a container starts so we need to use `CMD` not `RUN`.
