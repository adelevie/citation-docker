Docker image for the [citation.js](https://github.com/unitedstates/citation) library.

## How to use this image

First, `pull` the image:

```
docker pull adelevie/citation
```

### As a server

```
docker run -it --rm -p 3000:3000 adelevie/citation cite-server
```

This will expose the server to port `3000` on the host. To verify that it's working, run in another terminal window:

```
curl 'http://localhost:3000/citation/find?text=5+U.S.C.+552'
```

### As a CLI

Example:

```
docker run -it --rm -p 3000:3000 citation cite "section 5362(5) of title 31"
```

For more usage example, check out the README for citation.js
