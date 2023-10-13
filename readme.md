# devcontainer + Wagtail demo project

This is a demonstration project for using [devcontainers](https://code.visualstudio.com/docs/devcontainers/containers) with a non-trivial project based on the [Wagtail CMS](https://github.com/wagtail/wagtail).

📰 Read the post about this demo on [my blog: Isolated python environments with devcontainers](https://gremu.net/2023/devcontainer-as-pyenv-conda-alternative/)

## Setup

To get started:

1. Install [docker](https://docs.docker.com/engine/install/)
1. Install [Visual Studio Code](https://code.visualstudio.com/download) and the [devcontainer extension](https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-containers)
1. Checkout this repository: `git clone https://github.com/gregmuellegger/devcontainers-bakerydemo.git`
1. Open the folder with VS Code: `code ./devcontainers-bakerydemo`

Once VS Code started, it will offer you to "Reopen in Container".

After building the images, you need to run the following commands for initial setup:

```sh
python manage.py migrate
python manage.py load_initial_data
```

Now you are ready to run the server. Either execute or `python manage.py runserver` in the commandline, or press `F5` to run the server from within VS Code's debugger.

For more details see [the blog post](https://gremu.net/2023/devcontainer-as-pyenv-conda-alternative/).
