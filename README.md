# Guide found [here](https://nodejs.org/en/docs/guides/nodejs-docker-webapp/)
## Building
- build
```
docker build -t brendenvogt/node-web-app .
```
- verify
```
docker images
```

## Running
- run
```
docker run --name hello -p 49160:8080 -d brendenvogt/node-web-app
```
- verify
```
docker log hello
```
- what you should see
```
Running on http://0.0.0.0:8080
```

## Testing
- request
```
curl -i localhost:49160
```
- response
```
HTTP/1.1 200 OK
X-Powered-By: Express
Content-Type: text/html; charset=utf-8
Content-Length: 11
ETag: W/"b-Ck1VqNd45QIvq3AZd8XYQLvEhtA"
Date: Sat, 02 Jan 2021 10:03:40 GMT
Connection: keep-alive
Keep-Alive: timeout=5

Hello World
```

## Clean up 

```
docker stop hello
```

```
docker rm hello
```