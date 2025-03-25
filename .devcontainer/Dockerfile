FROM alpine
# 安装必要的软件包
RUN apk add --no-cache curl gcc
# 创建非 root 用户
RUN adduser -D codespace
USER codespace
WORKDIR /home/codespace
# 安装 Rust
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y --profile minimal --default-host x86_64-unknown-linuxmusl
# 设置环境变量
ENV PATH="/home/codespace/.cargo/bin:$PATH"
