# random-logger

## How do I use this image?

To use this image you must do as follows:

```bash
# you can use tags latest
docker pull local/random-logger:latest

# use different intervals to print logs every random(100, 400) milliseconds
docker run local/random-logger:latest 100 400

# use the third parameter so limit the number of loglines (after generating the lines the container will stop).
# if not set it runs infinite
docker run local/random-logger:latest 100 400 100

# to run the image just execute
docker run -d local/random-logger:latest
```

You will have now a docker container running and generating log messages, locate it running:

```bash
docker ps
```

You can see the logs using this command

```bash
docker logs <- container-id ->
```

## How do I build this images?

First things first, you can find these docker images in `local/random-logger`
but you can also build a specific version on your own, you only need:

* docker
* git

Clone this repo

`git clone https://github.com/local/random-logger.git`

Go to the folder in your terminal and type this:

```bash
# cd into folder
cd random-logger
# Then build the new image
docker build -f Dockerfile .
```

If you want to tag your image use the following command

```bash
docker build -f Dockerfile -t yourbase/yourname:version .
```

---

For more on docker build reference to the [Documentation](https://docs.docker.com/engine/reference/commandline/build/)

You can get the source from the image in the [Repository](https://github.com/local/random-logger)
