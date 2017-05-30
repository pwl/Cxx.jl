FROM julia:0.5.2

RUN apt-get update && \
    apt-get install -y --no-install-recommends \
    build-essential cmake libedit-dev libncurses5-dev python llvm llvm-dev && \
    rm -rf /var/lib/apt/lists/*

RUN mkdir /install
COPY install.jl /install
RUN julia -e 'include("/install/install.jl")'
