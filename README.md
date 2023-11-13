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

[blog]: https://sam.gleske.net/blog/engineering/2022/10/25/guide-to-production-docker-images.html
[debian]: https://hub.docker.com/_/debian
