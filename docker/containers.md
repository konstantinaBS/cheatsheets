## dockerized rstudio (rocker)

```
RSTUDIOPASS=<YOUR PASS>
docker run --rm -p 8787:8787 -e PASSWORD=$RSTUDIOPASS rocker/verse
```

This script will start a docker container of the rocker/verse image, downloading files as needed.

If you want to mount a host directory into docker:

```
RSTUDIOPASS=rstudio2 `you should use another one`
SOURCE_DIR="$(pwd)"/Workspace/brand-activation `<host directory to be mounted>`
DEST_DIR=/home/rstudio/app
docker run --rm -p 8787:8787 -e PASSWORD=$RSTUDIOPASS --name rocker -v $SOURCE_DIR:$DEST_DIR rocker/verse
```

When you see `[services.d] done` at the terminal, go to http://localhost:8787 and start using rstudio. Beware! The container will wipe everything once it's closed (`--rm` option)
