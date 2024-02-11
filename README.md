# README

This repository contains notes about the procedures for using `Dev Containers`.

## How to Create a Development Environment

1. Clone the repository: `git clone git@github.com:yuta-saito-0310/practice_devcontainer.git`
2. Copy `.env.sample` to `.env` and configure your environment variables
3. Build and run the Devcontainer:
    - If you use Dev Containers, which is an extension for VS Code:
        - Navigate to the `.devcontainer` directory: `cd .devcontainer`
        - Start the container: `docker compose up`
        - Connect to the application shell: `docker compose exec app /bin/bash`
        - Move to the project directory: `cd /workspaces/practice_devcontainer`
    - If you do not use Dev Containers, build and run the container with Docker Compose:
        - Navigate to the `.devcontainer` directory: `cd .devcontainer`
        - Start the container: `docker compose up`
        - Connect to the application shell: `docker compose exec app /bin/bash`
        - Move to the project directory: `cd /workspaces/practice_devcontainer`
4. Set up the database and install gems using `bin/setup`
5. Precompile assets with `rails assets:precompile` (since this repository uses Tailwind CSS)
6. Start the server with `rails s`