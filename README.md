# Llama_to_Llama.cpp

This project aims to create a guide for generating Llama.cpp GGUF model files out of base Llama v2 model weigths

## Getting Started

To run this project locally, you have two options:

- Use VS Code's Dev Container [Prefered].

- Create your own virtual environment.

### Using a Dev Container in VS Code

The Visual Studio Code Dev Containers extension lets you use a container as a full-featured development environment. It allows you to open any folder inside (or mounted into) a container and take advantage of Visual Studio Code's full feature set.

![image](https://code.visualstudio.com/assets/docs/devcontainers/containers/architecture-containers.png)

#### Requirements

- [ ] Docker installed locally.
- [ ] VS Code Dev Containers Extension.

        Name: Dev Containers
        Id: ms-vscode-remote.remote-containers
        Description: Open any folder or repository inside a Docker container and take advantage of Visual Studio Code's full feature set.
        Version: 0.347.0
        Publisher: Microsoft
        VS Marketplace Link: https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers

For more, please refer to: [System Requirements](https://code.visualstudio.com/docs/devcontainers/containers#_system-requirements)

#### Usage

If you meet the requirements, you can get started by just opening this project in VS Code, and selecting `Open in Dev Container`.

If the message above doesn't appear, you can press: `ctrl + shift + p` in your keyboard and type: `dev container`.
Select: `Open in Dev Container`.

This should display a status bar like example below:
![image](https://code.visualstudio.com/assets/docs/devcontainers/containers/dev-container-progress.png)

After the container starts successfully, you are ready to use and add features to the code.

### Create a Virtual Environment

Open the terminal and run the following commands:

1. Create virtual environment

    ```bash
    python -m venv .venv
    ```

2. Activate virtual environment

    - For Windows:

        ```powershell
        .venv/Scripts/activate
        ```

    - For Mac/Linux:

        ```bash
        source .venv/bin/activate
        ```

3. Install dependencies

    ```bash
    python -m pip install -r .devcontainer/requirements.txt
    ```

After the dependencies install successfully, you are ready to use and add features to the code.