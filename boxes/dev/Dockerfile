FROM quay.io/fedora/fedora:41

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

RUN <<EOT
  dnf check-update
  dnf install -y neovim-0.10.4-1.fc41 readline-devel-8.2-10.fc41
  dnf clean all
  rm -rf /var/cache/dnf/*
EOT
