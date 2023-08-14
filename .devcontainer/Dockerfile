FROM dart

RUN apt-get update && \
    apt-get install -y wget git unzip xz-utils zip libglu1-mesa && \
    apt-get clean && \
    cd / && \
    wget https://storage.googleapis.com/flutter_infra_release/releases/stable/linux/flutter_linux_3.10.6-stable.tar.xz && \
    tar xf flutter_linux_3.10.6-stable.tar.xz && \
    rm /flutter_linux_3.10.6-stable.tar.xz && \
    git config --global --add safe.directory /flutter

ENV PATH="/flutter/bin:$PATH"
RUN flutter doctor