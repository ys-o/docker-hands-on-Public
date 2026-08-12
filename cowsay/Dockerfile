# ベースにするイメージを指定
FROM ubuntu:latest

RUN apt-get update
RUN apt-get install cowsay -y

# ENTRYPOINT ["/usr/games/cowsay", "Hello, Docker!"]

# CMD ["/usr/games/cowsay", "Hello, Docker!"]

ENTRYPOINT ["/usr/games/cowsay"]
CMD ["Hello, Docker!"]
