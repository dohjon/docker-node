# docker-node

- [https://docs.npmjs.com/](https://docs.npmjs.com/)

## Usage

### Mac/Linux

**~/.bashrc** or **~/.bash_profiles**
```bash
node () {
    docker run \
        --rm \
        --workdir /custom \
        --volume $(pwd):/custom \
        dohjon/docker-node:latest \
        node "$@"
}

npm () {
    docker run \
        --rm \
        --workdir /custom \
        --volume $(pwd):/custom \
        dohjon/docker-node:latest \
        npm "$@"
}

npx () {
    docker run \
        --rm \
        --workdir /custom \
        --volume $(pwd):/custom \
        dohjon/docker-node:latest \
        npx "$@"
}
```

Debug
```bash
docker run \
    --interactive \
    --tty \
    --entrypoint /bin/sh
    --rm \
    --workdir /custom \
    --volume $(pwd):/custom \
    dohjon/docker-node:latest
```