FROM quay.io/fedora/fedora:41

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN <<EOT
  dnf check-update
  dnf install -y neovim readline-devel
  dnf clean all
  rm -rf /var/cache/dnf/*
  echo "something to trigger build cache"
EOT
