FROM docker.io/homebrew/ubuntu24.04:4.4.23

SHELL ["/bin/bash", "-o", "pipefail", "-c"]

USER root

RUN <<EOT
apt-get update
apt-get install \
  luarocks=3.8.0+dfsg1-1 \
  libmagickwand-dev=8:6.9.12.98+dfsg1-5.2build2 \
  libreadline-dev=8.2-4build1 \
  ripgrep=14.1.0-1 \
  wl-clipboard=2.2.1-1build1 \
  --no-install-recommends -y
apt-get clean
rm -rf /var/lib/apt/lists/*
EOT

USER linuxbrew

ENV HOMEBREW_NO_ANALYTICS=1 HOMEBREW_NO_AUTO_UPDATE=1 HOMEBREW_NO_ENV_HINTS=1

RUN <<EOT
brew install neovim mise zsh -f
brew cleanup -s

echo 'eval "$(mise activate bash)"' >> /home/linuxbrew/.zshrc
EOT

CMD ["/home/linuxbrew/.linuxbrew/bin/zsh"]
