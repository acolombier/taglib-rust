FROM mcr.microsoft.com/devcontainers/rust:latest
RUN sudo apt-get update && \
    sudo apt-get install -y cmake libutfcpp-dev unzip pkg-config clang && \
    wget -O taglib.zip https://github.com/taglib/taglib/archive/refs/tags/v2.2beta.zip && \
    unzip taglib.zip && \
    cmake -DCMAKE_INSTALL_PREFIX=/usr -DCMAKE_BUILD_TYPE=Release -DBUILD_SHARED_LIBS=OFF -DBUILD_TESTING=OFF taglib-2.2beta && \
    sudo make -j && \
    sudo make install