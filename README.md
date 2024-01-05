# Mlflow Docker Image - Mendel customized

This image is updated derrivative of https://github.com/burakince/mlflow

With updeted version of MLFlow to 2.9.2

Here is what specifically was changed

1. Change vesrion of python to 3.10
   1. In Dockerfile ``FROMpython:3.10.13AS foundation``
   2. In pyproject.toml
      ```
      python = "3.10.*"
      mlflow = {version = "2.9.2", extras = ["extras", "pipelines"]}
      ```

# How to build and push

```
docker build --platform linux/amd64 -t us-central1-docker.pkg.dev/mendel-health/softwares/mlflow . --push
```
