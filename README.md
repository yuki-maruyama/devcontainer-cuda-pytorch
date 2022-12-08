# DevContainer for CUDA + PyTorch 

This repository contains a [devcontainer](https://code.visualstudio.com/docs/remote/containers) for CUDA + PyTorch development. It is based on the [nvidia/cuda](https://hub.docker.com/r/nvidia/cuda) image.



## Features

You can use this devcontainer to develop CUDA + PyTorch applications in a container.

The container is based on the [nvidia/cuda](https://hub.docker.com/r/nvidia/cuda) image and contains the following tools:

- CUDA 11.7.1
- Python 3.10
- PyTorch
- Windows Subsystem for Linux 2 (WSL2)
  

## Usage

1. Install [Docker](https://docs.docker.com/get-docker/) and [VSCode](https://code.visualstudio.com/download).
2. Install the [Remote - Containers](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers) extension.
3. Clone this repository.
4. Open the repository in VSCode.
5. Click the green button in the lower left corner of the window.
6. Wait for the container to build and start.
7. Open a terminal in VSCode and run `python` to start the Python REPL.

## License

This project is licensed under the [MIT License](LICENSE).
