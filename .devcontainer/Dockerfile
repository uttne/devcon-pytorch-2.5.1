FROM pytorch/pytorch:2.5.1-cuda12.4-cudnn9-devel

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y git sudo
RUN rm -rf /var/lib/apt/lists/*

# vscode ユーザー作成
# -m : ホームディレクトリを作成
# -s : ログインシェルの指定（/bin/bash）
RUN useradd -m -s /bin/bash vscode
RUN echo "vscode ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

# 後続のコマンドを vscode ユーザー権限で実行
USER vscode

WORKDIR /workspace
