FROM archlinux
# base build
RUN echo 'Server = http://mirrors.pku.edu.cn/archlinux/$repo/os/$arch' > /etc/pacman.d/mirrorlist
RUN pacman -Syu --noconfirm
RUN pacman -S base-devel --noconfirm
RUN pacman -S neovim python-pynvim --noconfirm
RUN pacman -S tmux bash-completion zsh --noconfirm
RUN pacman -S git wget net-tools unzip --noconfirm
RUN pacman -S cmake gdb --noconfirm
# add archlinuxcn
RUN echo '[archlinuxcn]' >> /etc/pacman.conf
RUN echo 'Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch' >> /etc/pacman.conf
RUN pacman -Sy archlinuxcn-keyring --noconfirm
RUN rm -R /etc/pacman.d/gnupg
RUN pacman-key --init
RUN pacman-key --populate archlinux
RUN pacman-key --populate archlinuxcn
RUN pacman -S yay --noconfirm
RUN pacman -S neovim-symlinks --noconfirm
# use config
RUN sed -i 's/# %wheel ALL=(ALL:ALL) ALL/%wheel ALL=(ALL:ALL) ALL/' /etc/sudoers
RUN useradd -m -s /bin/zsh jxm2001
RUN usermod -aG wheel jxm2001
RUN echo jxm2001:jxm2001 | chpasswd
USER jxm2001
WORKDIR /home/jxm2001
CMD /bin/bash
