# Gemini CLI Dev Container
[![run_devcontainer_ci](https://github.com/codequokka/devcontainer-gemini-cli/actions/workflows/run_devcontainer_ci.yaml/badge.svg)](https://github.com/codequokka/devcontainer-gemini-cli/actions/workflows/run_devcontainer_ci.yaml)
[![run_github_actions_workflow_ci](https://github.com/codequokka/devcontainer-gemini-cli/actions/workflows/run_github_actions_workflow_ci.yml/badge.svg)](https://github.com/codequokka/devcontainer-gemini-cli/actions/workflows/run_github_actions_workflow_ci.yml)

This repository provides a pre-configured development environment using [VS Code Dev Containers](https://code.visualstudio.com/docs/devcontainers/containers) to easily get started with the [Google Gemini CLI](https://github.com/google/gemini-cli).

It allows you to use the Gemini CLI in a sandboxed, consistent, and reproducible environment without needing to install `npm` or other dependencies directly on your host machine.

## Features

- **Zero Configuration**: Just open this repository in a Dev Container and you're ready to go.
- **Isolated Environment**: The Gemini CLI and its dependencies are installed inside a Docker container, keeping your local system clean.
- **Reproducible**: Ensures everyone on a team has the exact same development environment.
- **Pre-installed Tools**: Comes with `@google/gemini-cli` ready to use.

## Getting Started

### Prerequisites

- [Docker](https://www.docker.com/products/docker-desktop/)
- [Visual Studio Code](https://code.visualstudio.com/)
- [VS Code Dev Containers extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)

### Quick Start

1.  Clone this repository to your local machine.
2.  Open the repository folder in Visual Studio Code.
3.  When prompted, click on **"Reopen in Container"**. This will build the Docker container and set up the environment.

Once the Dev Container is up and running, you can start using the Gemini CLI.

## Authentication

You need to authenticate with your Google account to use the Gemini CLI. The following commands should be run in the VS Code terminal.

### 1. Login with Google

Execute the `gemini` command to start the authentication process:

```bash
gemini
```

Select `1. Login with Google` from the menu. You might be asked to follow a URL and enter a verification code to complete the login.

### 2. Use a Gemini API Key

If you prefer to use an API key:

1.  [Get your Gemini API Key](https://aistudio.google.com/apikey) from Google AI Studio.
2.  Run the `gemini` command:

    ```bash
    gemini
    ```

3.  Select `2. Use Gemini API Key` and paste your key when prompted.

## Customization

You can customize this development environment by editing the files in the `.devcontainer` directory.

-   **`.devcontainer/devcontainer.json`**: Add more VS Code extensions or change container settings.
-   **`.devcontainer/gemini-cli/Dockerfile`**: Add or remove system-level dependencies.
-   **`.devcontainer/gemini-cli/postCreateCommand.sh`**: Add commands to install additional tools or CLIs after the container is created. For example, you can add more packages to be installed with `aqua`.
