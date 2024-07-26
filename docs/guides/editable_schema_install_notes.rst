**Setup protoc and protobuf-javascript**

To install protoc and protobuf-javascript in Ubuntu, run the following from your home directory:

.. code-block::

    mkdir protoc
    cd protoc
    wget https://github.com/protocolbuffers/protobuf/releases/download/v22.3/protoc-22.3-linux-x86_64.zip
    unzip protoc-22.3-linux-x86_64.zip
    wget https://github.com/protocolbuffers/protobuf-javascript/releases/download/v3.21.2/protobuf-javascript-3.21.2-linux-x86_64.zip
    unzip protobuf-javascript-3.21.2-linux-x86_64.zip
    PATH=$GITHUB_WORKSPACE/protoc/bin:$PATH protoc --version

To install Go (Golang) in Ubuntu WSL, run the following from your home directory:

.. code-block::

    wget https://go.dev/dl/go1.22.5.linux-amd64.tar.gz
    sudo rm -rf /usr/local/go && sudo tar -C /usr/local -xzf go1.22.5.linux-amd64.tar.gz
    export PATH=$PATH:/usr/local/go/bin
