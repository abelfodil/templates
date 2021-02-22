FROM mcr.microsoft.com/vscode/devcontainers/base:ubuntu-20.04

RUN apt update \
    && apt install -y build-essential bzip2 clang clang-format clang-tidy cmake cowsay cppcheck fish git iputils-ping libncurses5 ninja-build openocd picocom python3-pip wget \
    && apt-get autoremove -y && apt-get clean -y && rm -rf /var/lib/apt/lists/*

WORKDIR /binaries

RUN wget -qO- https://developer.arm.com/-/media/Files/downloads/gnu-rm/10-2020q4/gcc-arm-none-eabi-10-2020-q4-major-x86_64-linux.tar.bz2 | tar -xj
ENV PATH "/binaries/gcc-arm-none-eabi-10-2020-q4-major/bin:$PATH"

RUN ln -nfs /usr/bin/python3 /usr/bin/python

ENV PATH "/usr/games:$PATH"
