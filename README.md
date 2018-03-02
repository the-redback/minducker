# MinDucker

MinDucker (or, _`Minikube Docker Sucker`_ :p) is a teeny-tiny script that carries over docker images from local machine to Minikube.

## Usage

This script does the following:

- Carries over docker images from local machine to Minikube.
- Useful for private docker images. No hassels of creating `ImagePullSecret` for kubernetes.
- Removes dangling images created by new image.

## One command to rule them all!

```console
$ minducker <image-name>
```

## Set Me UP!

Move this Script in to your path

```console
$ curl -LO https://raw.githubusercontent.com/the-redback/min-ducker/master/minducker \
  && chmod +x ./minducker \
  && sudo mv ./minducker /usr/local/bin/minducker
```

## Script in Action!

```console
$ minducker the-redback/apiserver

REPOSITORY              TAG                 IMAGE ID            CREATED             SIZE
the-redback/apiserver   0.0.3               8043a69a5c9c        8 minutes ago       70.6 MB
the-redback/apiserver   0.0.1               e905a87e116d        2 months ago        360 MB
the-redback/apiserver   0.0.2               e905a87e116d        2 months ago        360 MB

cd7100a72410: Loading layer 4.403 MB/4.403 MB
a57da7ccb184: Loading layer 2.059 MB/2.059 MB
c916a1ee8141: Loading layer 64.64 MB/64.64 MB
...

Loaded image: the-redback/apiserver:0.0.1
Loaded image: the-redback/apiserver:0.0.2
Loaded image: the-redback/apiserver:0.0.3
```

**_Happy Hacking! B|_**
