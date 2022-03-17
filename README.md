# Fast API Starter

- author : Anthony Leotta
- started : March 16, 2022
- tags : FastAPI, SQLAlchemy, PostgreSQL, Alembic, Docker
- about : The purpose of this repo is to create a simple starter project that can be used as a guide on how to use FastAPI with SQLAlchemy and migrations.
- credits : I list all the articles I read and repos in the Resources section.

## Goals

I've been using Flask, Django for many years and PHP before those.  When learning a new framework I find its best to create a few projects and try out the features before you start on something real.

- Manage Python virtual environments with PyEnv
- Manage Python packages using Poetry
- FastAPI running inside a Docker container
- Use latest PostgreSQL version
- SQL Alchemy for database access
- Alembic for schema migrations
    - Automate the initial migration
    - Can migrations be run each time the container is built? Is that even a good idea?
- PyTest unit tests
    - Create and destroy a test database

## Dependencies

1. [Python]()
1. [PyEnv](https://github.com/pyenv/pyenv)
1. [Poetry](https://python-poetry.org/docs/)
1. [Fastapi]()
1. [Pydantic]()
1. [Fastapi-sqlalchemy]()
1. [Alembic]()
1. [Psycopg2]()
1. [Uvicorn]()

## Pyenv Installation

1. See this list [OS-specific dependencies](https://github.com/pyenv/pyenv/wiki#suggested-build-environment)

1. Install Ubuntu/Linux OS-specific dependencies

    ```
    sudo apt-get install -y make build-essential libssl-dev zlib1g-dev \
    libbz2-dev libreadline-dev libsqlite3-dev wget curl llvm libncurses5-dev \
    libncursesw5-dev xz-utils tk-dev libffi-dev liblzma-dev python-openssl
    ```

1. Install PyEnv with pyenv-installer

    ```
    curl https://pyenv.run | bash
    ```

1. Add .pyenv to .bashrc

    ```
    export PYENV_ROOT="$HOME/.pyenv"
    export PATH="$PYENV_ROOT/bin:$PATH"
    if command -v pyenv 1>/dev/null 2>&1; then
    eval "$(pyenv init --path)"
    fi
    ```

1. Check if PyEnv is installed


    ```
    pyenv --version
    ```

    On my system it returns: pyenv 2.2.5


1. List all the Python version that pyenv supports

    ```
    pyenv install --list
    ```

1. I am installing Python 3.10

    ```
    pyenv install 3.10.3
    ```

    ```
    Downloading Python-3.10.3.tar.xz...
    -> https://www.python.org/ftp/python/3.10.3/Python-3.10.3.tar.xz
    Installing Python-3.10.3...
    Installed Python-3.10.3 to /home/tonyl/.pyenv/versions/3.10.3
    ```
1. Set the default global python

    ```
    pyenv global 3.10.3
    ```

1. Check which Python is enabled

    ```
    python --version
    ```

    which returns

    ```
    Python 3.10.3
    ```

1. Check PyEnv Versions

    ```
    pyenv versions
    ```

    which returns

    ```
    system
    * 3.10.3 (set by /home/tonyl/.pyenv/version)
    ```

## Poetry Installation

1. Install

    ```
    curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python -
    ```

1. Check Installation

    ```
    poetry --version
    ```

    which returns

    ```
    Poetry version 1.1.13
    ```




## Resources

1. [Modern Python part 1: start a project with pyenv & poetry](https://www.adaltas.com/en/2021/06/09/pyrepo-project-initialization/)
1. [FastAPI with SQLAlchemy, PostgreSQL and Alembic and of course Docker [Part-1]](https://ahmed-nafies.medium.com/fastapi-with-sqlalchemy-postgresql-and-alembic-and-of-course-docker-f2b7411ee396)