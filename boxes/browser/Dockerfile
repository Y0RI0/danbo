FROM docker.io/library/archlinux:base-devel

# makepkg user and workdir
ARG user=makepkg
RUN <<EOT
 pacman -Syu --needed --noconfirm git
 useradd --system --create-home $user
 echo "$user ALL=(ALL:ALL) NOPASSWD:ALL" > /etc/sudoers.d/$user
EOT

USER $user
WORKDIR /home/$user
# Install yay
RUN <<EOT
  git clone https://aur.archlinux.org/yay.git 
  sh -c "cd /home/makepkg/yay && makepkg -sri --needed --noconfirm"
  yay -S floorp --noconfirm
  rm -rf .cache yay
EOT
