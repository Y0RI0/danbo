FROM quay.io/fedora/fedora:41

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

# https://discussion.fedoraproject.org/t/fedora-38-github-action-throttling/80393/6
RUN <<EOT
  dnf --disablerepo=fedora-cisco-openh264 install -y neovim-0.10.4-1.fc41 readline-devel-8.2-10.fc41
  dnf clean all
  rm -rf /var/cache/dnf/*
  rm -rf /var/cache/yum
EOT
