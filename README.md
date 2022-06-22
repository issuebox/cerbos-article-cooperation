# cerbos-article-cooperation
An Article Collaboration System Permission Design With Cerbos

## start cerbos service
```bash
docker run --rm --name cerbos -d -v $(pwd)/policies:/policies -p 3592:3592 ghcr.io/cerbos/cerbos:0.18.0
```


## test cerbos policies
```bash
docker run -i -t -v $(pwd)/policies:/policies -v $(pwd)/tests:/tests ghcr.io/cerbos/cerbos:0.18.0 compile --tests=/tests /policies
```