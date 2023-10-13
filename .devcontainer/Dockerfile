FROM mcr.microsoft.com/devcontainers/python:1-3.9-bullseye

# We can install more devtools which wouldn't be included in any production
# docker image.
RUN sudo apt update && sudo apt install -yy cowsay

# Install requirements. We don't need a virtualenv, as we only have this one project in the container.
ADD requirements/ /requirements/
RUN pip install -r /requirements/production.txt -r /requirements/development.txt
