# Glenna Project Documentation

## Create documentation using Docker

### Pull docker image

    docker pull plaindocs/docker-sphinx

### Use Make to build PDF document

    docker run -i -v $PWD/docs:/documents/ plaindocs/docker-sphinx make latexpdf

### Created documents

Can be found at

    docs/_build/
