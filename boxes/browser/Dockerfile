## Testing
FROM docker.io/library/ubuntu:24.04

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

RUN <<EOT
  apt-get update
  apt-get install -y --no-install-recommends gnupg2=2.4.4-2ubuntu17 curl=8.5.0-2ubuntu10.6

  curl -fsSL https://ppa.floorp.app/KEY.gpg | gpg --dearmor -o /usr/share/keyrings/Floorp.gpg
  curl -sS --compressed -o /etc/apt/sources.list.d/Floorp.list "https://ppa.floorp.app/Floorp.list"
  apt-get install -y --no-install-recommends floorp=11.24.0
  
  apt-get clean
  rm -rf /var/lib/apt/lists/*
EOT

USER ubuntu
