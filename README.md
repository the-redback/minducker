# MinDucker

MinDucker (or, `Minikube Sucker` :p) is a teeny-tiny script that carries over docker images from host machine to Minikube.

This script does the following:

- Carries over docker images from host machine to Minikube.
- Removes dangling images created by new image.

## Set Me UP!

Move Script in to your path

```console
$ curl -LO https://raw.githubusercontent.com/the-redback/min-ducker/master/minducker \
  && chmod +x ./minducker \
  && sudo mv ./minducker /usr/local/bin/minducker
```

## Usage

```console
$ minducker <imagename>
```

## Script in Action!

```console
$ minducker the-redback/apiserver
REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
the-redback/apiserver   0.0.1               c54e42630fc5        9 days ago          69.6 MB
cd7100a72410: Loading layer 4.403 MB/4.403 MB
11e956666842: Loading layer 2.058 MB/2.058 MB
b9b8fcbaedcd: Loading layer 63.68 MB/63.68 MB
Loaded image: the-redback/apiserver:0.0.1
```

**_Happy Hacking! B|_**
