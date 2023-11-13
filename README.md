# Distroless Docker Images

When building distroless you should do it yourself rather than relying on a 3rd
party to provide "distroless".

These images are based off of [an article][blog] I wrote and all of the
companion articles contained within its sources.

# Debian

Build off of the latest available [Debian docker image][debian].

    docker build -t distroless-debian -f Dockerfile.debian .

Build a specific version of Debian.

    docker build --build-arg debian=11 -t distroless-debian -f Dockerfile.debian .

# Amazon Linux 2023

Build a minimal distroless version of `amazonlinux:2023` with
[`Dockerfile.amazonlinux2023`](Dockerfile.amazonlinux2023).

    docker build -t distroless-al23 -f Dockerfile.amazonlinux2023 .

### Java distroless

Also based on Amazon Linux 2023.

    docker build -t distroless-al23-java21 -f Dockerfile.amazonlinux2023-java .

Or building alternate versions of Java.

    docker build --build-arg java=11 -t distroless-al23-java11 -f Dockerfile.amazonlinux2023-java .
    docker build --build-arg java=17 -t distroless-al23-java17 -f Dockerfile.amazonlinux2023-java .

[blog]: https://sam.gleske.net/blog/engineering/2022/10/25/guide-to-production-docker-images.html
[debian]: https://hub.docker.com/_/debian
