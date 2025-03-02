Learn about how to self-host Khoj on your own machine.

Benefits to self-hosting:

1. **Privacy**: Your data will never have to leave your private network. You can even use Khoj without an internet connection if deployed on your personal computer.
2. **Customization**: You can customize Khoj to your liking, from models, to host URL, to feature enablement.

## Setup Khoj[​](#setup-khoj "Direct link to Setup Khoj")

These are the general setup instructions for self-hosted Khoj. You can install the Khoj server using either [Docker](https://docs.khoj.dev/get-started/setup/?server=docker) or [Pip](https://docs.khoj.dev/get-started/setup/?server=pip).

Offline Model + GPU

To use the offline chat model with your GPU, we recommend using the Docker setup with Ollama . You can also use the local Khoj setup via the Python package directly.

First Run

Restart your Khoj server after the first run to ensure all settings are applied correctly.

- Docker
- Pip

- MacOS
- Windows
- Linux

### Prerequisites

#### Docker

- _Option 1_: Click here to install [Docker Desktop](https://docs.docker.com/desktop/install/mac-install/). Make sure you also install the [Docker Compose](https://docs.docker.com/desktop/install/mac-install/) tool.
    
- _Option 2_: Use [Homebrew](https://brew.sh/) to install Docker and Docker Compose.
    
    ```
    brew install --cask dockerbrew install docker-compose
    ```
    

### Setup

1. Download the Khoj docker-compose.yml file [from Github](https://github.com/khoj-ai/khoj/blob/master/docker-compose.yml)
    
    ```
    mkdir ~/.khoj && cd ~/.khojwget https://raw.githubusercontent.com/khoj-ai/khoj/master/docker-compose.yml
    ```
    
2. Configure the environment variables in the `docker-compose.yml`
    - Set `KHOJ_ADMIN_PASSWORD`, `KHOJ_DJANGO_SECRET_KEY` (and optionally the `KHOJ_ADMIN_EMAIL`) to something secure. This allows you to customize Khoj later via the admin panel.
    - Set `OPENAI_API_KEY`, `ANTHROPIC_API_KEY`, or `GEMINI_API_KEY` to your API key if you want to use OpenAI, Anthropic or Gemini commercial chat models respectively.
    - Uncomment `OPENAI_BASE_URL` to use [Ollama](https://docs.khoj.dev/advanced/ollama?type=first-run&server=docker#setup) running on your host machine. Or set it to the URL of your OpenAI compatible API like vLLM or [LMStudio](https://docs.khoj.dev/advanced/lmstudio).
3. Start Khoj by running the following command in the same directory as your docker-compose.yml file.
    
    ```
    cd ~/.khojdocker-compose up
    ```
    

Remote Access

By default Khoj is only accessible on the machine it is running. To access Khoj from a remote machine see [Remote Access Docs](https://docs.khoj.dev/advanced/remote).

Your setup is complete once you see `🌖 Khoj is ready to use` in the server logs on your terminal.

## Use Khoj[​](#use-khoj "Direct link to Use Khoj")

You can now open the web app at [http://localhost:42110](http://localhost:42110/) and start interacting!  
Nothing else is necessary, but you can customize your setup further by following the steps below.

First Message to Offline Chat Model

The offline chat model gets downloaded when you first send a message to it. The download can take a few minutes! Subsequent messages should be faster.

### Add Chat Models[​](#add-chat-models "Direct link to Add Chat Models")

#### Login to the Khoj Admin Panel

Go to [http://localhost:42110/server/admin](http://localhost:42110/server/admin) and login with the admin credentials you setup during installation.

CSRF Error

Ensure you are using **localhost, not 127.0.0.1**, to access the admin panel to avoid the CSRF error.

CSRF Trusted Origin or Unset Cookie Error

If using a load balancer/reverse_proxy in front of your Khoj server: Set the environment variable KHOJ_ALLOWED_DOMAIN=your-internal-ip-or-domain to avoid this error. If unset, it defaults to KHOJ_DOMAIN.

DISALLOWED HOST or Bad Request (400) Error

You may hit this if you try access Khoj exposed on a custom domain (e.g. 192.168.12.3 or example.com) or over HTTP. Set the environment variables KHOJ_DOMAIN=your-external-ip-or-domain and KHOJ_NO_HTTPS=True if required to avoid this error.

Note

Using Safari on Mac? You might not be able to login to the admin panel. Try using Chrome or Firefox instead.

#### Configure Chat Model

Setup which chat model you'd want to use. Khoj supports local and online chat models.

- OpenAI
- Anthropic
- Gemini
- Offline

Ollama Integration

Using Ollama? See the [Ollama Integration](https://docs.khoj.dev/advanced/ollama) section for more custom setup instructions.

1. Create a new [AI Model Api](http://localhost:42110/server/admin/database/aimodelapi/add) in the server admin settings.
    - Add your [OpenAI API key](https://platform.openai.com/api-keys)
    - Give the configuration a friendly name like `OpenAI`
    - (Optional) Set the API base URL. It is only relevant if you're using another OpenAI-compatible proxy server like [Ollama](https://docs.khoj.dev/advanced/ollama) or [LMStudio](https://docs.khoj.dev/advanced/lmstudio).  
        ![example configuration for ai model api](https://docs.khoj.dev/assets/images/example_openai_processor_config-36379d7131acabbf7c8c3b4cdeae5c88.png)
2. Create a new [chat model](http://localhost:42110/server/admin/database/chatmodel/add)
    - Set the `chat-model` field to an [OpenAI chat model](https://platform.openai.com/docs/models). Example: `gpt-4o`.
    - Make sure to set the `model-type` field to `OpenAI`.
    - If your model supports vision, set the `vision enabled` field to `true`. This is currently only supported for OpenAI models with vision capabilities.
    - The `tokenizer` and `max-prompt-size` fields are optional. Set them only if you're sure of the tokenizer or token limit for the model you're using. Contact us if you're unsure what to do here.  
        ![example configuration for chat model options](https://docs.khoj.dev/assets/images/example_chatmodel_option-a17ba2304283d01e547d7e9727056969.png)

Multiple Chat Models

Set your preferred default chat model in the `Default`, `Advanced` fields of your [ServerChatSettings](http://localhost:42110/server/admin/database/serverchatsettings/). Khoj uses these chat model for all intermediate steps like intent detection, web search etc.

Chat Model Fields

- The `tokenizer` and `max-prompt-size` fields are optional. Set them only if you're sure of the tokenizer or token limit for the model you're using. This improves context stuffing. Contact us if you're unsure what to do here.
- Only tick the `vision enabled` field for OpenAI models with vision capabilities like gpt-4o. Vision capabilities in other chat models is not currently utilized.

### Sync your Knowledge[​](#sync-your-knowledge "Direct link to Sync your Knowledge")

- You can chat with your notes and documents using Khoj.
- Khoj can keep your files and folders synced using the Khoj [Desktop](https://docs.khoj.dev/clients/desktop#setup), [Obsidian](https://docs.khoj.dev/clients/obsidian#setup) or [Emacs](https://docs.khoj.dev/clients/emacs#setup) clients.
- Your [Notion workspace](https://docs.khoj.dev/data-sources/notion_integration) can be directly synced from the web app.
- You can also just drag and drop specific files you want to chat with on the [Web app](https://docs.khoj.dev/clients/web#upload-documents).

### Setup Khoj Clients[​](#setup-khoj-clients "Direct link to Setup Khoj Clients")

The Khoj web app is available by default to chat, search and configure Khoj.  
You can also install a Khoj client to easily access it from Obsidian, Emacs, Whatsapp or your OS and keep your documents synced with Khoj.

Note

Set the host URL on your clients settings page to your Khoj server URL. By default, use `http://127.0.0.1:42110` or `http://localhost:42110`. Note that `localhost` may not work in all cases.

- Desktop
- Emacs
- Obsidian
- Whatsapp

- Read the Khoj Desktop app [setup docs](https://docs.khoj.dev/clients/desktop#setup).

## Upgrade[​](#upgrade "Direct link to Upgrade")

### Upgrade Server[​](#upgrade-server "Direct link to Upgrade Server")

- Pip
- Docker

Run the commands below from the same directory where you have your `docker-compose.yml` file. This will fetch the latest build and upgrade your server.

```
# Windows users should use their WSL2 terminal to run these commandscd ~/.khoj  # assuming your khoj docker-compose.yml file is heredocker-compose up --build
```

### Upgrade Clients[​](#upgrade-clients "Direct link to Upgrade Clients")

- Desktop
- Emacs
- Obsidian

- The Desktop app automatically updates to the latest released version on restart.
- You can manually download the latest version from the [Khoj Website](https://khoj.dev/downloads).

## Uninstall[​](#uninstall "Direct link to Uninstall")

### Uninstall Server[​](#uninstall-server "Direct link to Uninstall Server")

- Pip
- Docker

Run the command below from the same directory where you have your `docker-compose` file. This will remove the server containers, networks, images and volumes.

```
docker-compose down --volumes
```

### Uninstall Clients[​](#uninstall-clients "Direct link to Uninstall Clients")

- Desktop
- Emacs
- Obsidian

Uninstall the Khoj Desktop client in the standard way from your OS.

## Troubleshoot[​](#troubleshoot "Direct link to Troubleshoot")

#### Dependency conflict when trying to install Khoj python package with pip[​](#dependency-conflict-when-trying-to-install-khoj-python-package-with-pip "Direct link to Dependency conflict when trying to install Khoj python package with pip")

- **Reason**: When conflicting dependency versions are required by Khoj vs other python packages installed on your system
- **Fix**: Install Khoj in a python virtual environment using [venv](https://docs.python.org/3/library/venv.html) or [pipx](https://pypa.github.io/pipx) to avoid this dependency conflicts
- **Process**:
    1. Install [pipx](https://pypa.github.io/pipx/#install-pipx)
    2. Use `pipx` to install Khoj to avoid dependency conflicts with other python packages.
    3. Now start `khoj` using the standard steps described earlier

#### Install fails while building Tokenizer dependency[​](#install-fails-while-building-tokenizer-dependency "Direct link to Install fails while building Tokenizer dependency")

- **Details**: `pip install khoj` fails while building the `tokenizers` dependency. Complains about Rust.
- **Fix**: Install Rust to build the tokenizers package. For example on Mac run:
    
    ```
    brew install rustuprustup-initsource ~/.cargo/env
    ```
    
- **Refer**: [Issue with Fix](https://github.com/khoj-ai/khoj/issues/82#issuecomment-1241890946) for more details

#### Khoj in Docker errors out with "Killed" in error message[​](#khoj-in-docker-errors-out-with-killed-in-error-message "Direct link to Khoj in Docker errors out with \"Killed\" in error message")

- **Fix**: Increase RAM available to Docker Containers in Docker Settings
- **Refer**: [StackOverflow Solution](https://stackoverflow.com/a/50770267), [Configure Resources on Docker for Mac](https://docs.docker.com/desktop/mac/#resources)