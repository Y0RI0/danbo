## Testing
FROM docker.io/library/ubuntu:24.04

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

RUN <<EOT
  # Add the GPG keys to your system
  curl -fsSL https://ppa.floorp.app/KEY.gpg | gpg --dearmor -o /usr/share/keyrings/Floorp.gpg

  # Add the repository to your system
  curl -sS --compressed -o /etc/apt/sources.list.d/Floorp.list "https://ppa.floorp.app/Floorp.list"

  # Update the package list and install Floorp
  apt-get update
  apt-get install -y --no-install-recommends floorp=11.24.0
  apt-get clean
  rm -rf /var/lib/apt/lists/*
EOT

USER ubuntu
