
# docker instructions

## build images

build the cli image:
```sh
docker build --pull -t aitg_host -f docker/Dockerfile .
```

## run images

run cli:
```sh
docker run -it --rm -v $(pwd)/models/YOUR_MODEL:/app/model aitg_host aitg_host.cli
```

run server:
```sh
docker run -it --rm -v $(pwd)/models/YOUR_MODEL:/app/model -e KEY=secret -p 6000:6000 aitg_host aitg_host.srv --host 0.0.0.0
```
