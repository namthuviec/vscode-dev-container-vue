# Vue (Vue CLI Dev Container)

## Summary

*Develop Vue.js 3 applications with Vue CLI inside a fully containerized development environment. Includes Node.js, Vue CLI, ESLint, and recommended VS Code extensions.*

|          Metadata           |                    Value                     |
| --------------------------- | -------------------------------------------- |
| *Contributors*              | [ngnam](https://github.com/ngnam) |
| *Definition type*           | Docker Compose + Dockerfile                  |
| *Works in Codespaces*       | Yes                                          |
| *Container host OS support* | Linux, macOS, Windows                        |
| *Languages, platforms*      | TypeScript, JavaScript (optional)            |

## Features

- Node.js 18 LTS base image  
- Vue CLI (`@vue/cli`, `@vue/cli-service-global`) preinstalled  
- ESLint + Volar (Vue 3) extensions for VS Code  
- Hot reload via volume mounting  
- Debugging support (Node inspector on port `9229`)  
- npm/yarn cache volumes for faster installs  

## Using this definition with an existing folder

1. If this is your first time using a development container, please follow the [getting started steps](https://aka.ms/vscode-remote/containers/getting-started) to set up your machine.

2. To use this definition:
   1. Start VS Code and open your project folder.
   2. Ensure you have the `.devcontainer` folder (with `Dockerfile`, `docker-compose.yml`, and `devcontainer.json`) in your project.
   3. Press <kbd>F1</kbd>, select **Dev Containers: Reopen in Container**.

3. The container will build and install dependencies automatically (`npm install` via `postCreateCommand`).

4. Once running, your Vue app will be available at [http://localhost:8080](http://localhost:8080).

## Debugging

- The container exposes port **9229** for Node.js debugging.  
- You can attach VS Code’s debugger using a `launch.json` configuration.  

## License

Copyright (c) Microsoft Corporation.  
Licensed under the MIT License. See [LICENSE](https://github.com/Microsoft/vscode-dev-containers/blob/master/LICENSE).
