# Hello Dagger test

This repository contains a simple Vuejs app using Dagger as pipeline scripting engine for learning pourposes.

## Useful Dagger commands

- To initialize Dagger in the current project.

  sdk: Indicates the language is going to be used for Dagger.

  source: The output directory for Dagger files.

```bash
dagger init --sdk=python --source=./dagger
```

- Execute a Dagger function

```bash
dagger call FUNTION-KEBAB-NAME  --source=.
```

- Debug Just-in-time container (Artifcat generated in function that returns a Container type).

```bash
dagger call build-env --source=. terminal --cmd=bash
```

- Start a just-in-time container as a local service and forward any exposed ports to host machine.

  This is like a docker compose up but in code.

```bash
dagger call build --source=. as-service up --ports=8080:80
```
