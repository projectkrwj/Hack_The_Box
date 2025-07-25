FROM ubuntu:22.04

ENV DEBIAN_FRONTEND=noninteractive

# 기본 패키지 설치
RUN apt update && apt install -y \
    python3 python3-pip python3-dev \
    gdb git curl wget unzip \
    gcc g++ make cmake \
    nano tmux zsh \
    libssl-dev libffi-dev \
    && rm -rf /var/lib/apt/lists/*

# pwndbg 설치
RUN git clone https://github.com/pwndbg/pwndbg /opt/pwndbg && \
    cd /opt/pwndbg && ./setup.sh
