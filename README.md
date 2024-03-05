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

### Download model from Hugging Face

#### Requirements

- [ ] Hugging Face account.
    
    Can be created [here](https://huggingface.co/join).

- [ ] Hugging Face API Token.

    Can be requested [here](https://huggingface.co/settings/tokens).

- [ ] Request access to Meta's Llama v2 models

    Can be requested [here](https://huggingface.co/meta-llama/Llama-2-7b-chat-hf).

> :memo: **NOTE**: A Hugging Face Token is need to access gated models like `Llama v2` and to authenticate with the Hugging Face CLI.

To download a model from Hugging Face, run the notebook [Model Downloader](./model_downloader.ipynb).

The output of this notebook should the desired Hugging Face model inside the `models` directory.

![image](https://github.com/kevinknights29/Llama_to_Llama.cpp/assets/74464814/d46f9124-9b95-4d6a-88ff-982234852865)

### Generating a GGUF file from Hugging Face Llama model weights

To convert the download Llama model from step above, run the notebook [GGUF Converter](./GGUF_converter.ipynb).

This cell is responsible of converting the model to a GGUF compatible format.

![image](https://github.com/kevinknights29/Llama_to_Llama.cpp/assets/74464814/d3a84ea8-8672-4c79-81e8-cef7296168ee)

The remaining part of the notebook will quantize the model (to reduce memory foot print - but may cause response quality degradation) and upload to Hugging Face.

![image](https://github.com/kevinknights29/Llama_to_Llama.cpp/assets/74464814/328fe6d5-a22b-427e-85b6-eb1f0418ecf1)

#### Upload to Hugging Face

![image](https://github.com/kevinknights29/Llama_to_Llama.cpp/assets/74464814/e03d78b9-b113-4ab9-a39d-12c9f74ca2e2)

![image](https://github.com/kevinknights29/Llama_to_Llama.cpp/assets/74464814/4d99465c-b47d-48fa-afd1-72dd8016210c)

Repo: [kevinknights29/llama-2-7b-chat-q4_0.gguf](https://huggingface.co/kevinknights29/llama-2-7b-chat-q4_0.gguf/tree/main)