# go-docker

Run
```
CGO_ENABLED=0 goos="linux" go build   # create go-docker executable
./run                                 # copy executable into alpine container and run it
```

Run only the go container
```
docker run -it godocker_server sh
./go-docker
```

Building inside alpine
```
docker build -t go-server .
docker run --rm -it -p 3000:3000 go-server ./go-docker
```

