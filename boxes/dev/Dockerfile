# Testing
FROM docker.io/library/ubuntu:24.04

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

RUN <<EOT
  apt-get update
  apt-get install -y --no-install-recommends bashtop
  apt-get clean
  rm -rf /var/lib/apt/lists/*
EOT

ENV PYTHONUNBUFFERED=1

USER ubuntu
