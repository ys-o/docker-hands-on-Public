# ベースにするイメージを指定
FROM ubuntu:latest




# RUNで、パッケージ情報更新＋cowsay導入
# RUN apt-get update
# RUN apt-get install cowsay -y

# @レイヤー削減＋不要なファイルの削除
RUN apt-get update \
  && apt-get install cowsay -y \
  && rm -rf /var/lib/apt/lists/*



# @ENTRYPOINTのみ
# ENTRYPOINT ["/usr/games/cowsay", "Hello, Docker!"]

# @CMDのみ
# CMD ["/usr/games/cowsay", "Hello, Docker!"]

# @組み合わせ
ENTRYPOINT ["/usr/games/cowsay"]
CMD ["Hello, Docker!"]
