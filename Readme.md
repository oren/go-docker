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
