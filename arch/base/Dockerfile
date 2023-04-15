FROM archlinux
# base build
RUN echo 'Server = http://mirrors.pku.edu.cn/archlinux/$repo/os/$arch' > /etc/pacman.d/mirrorlist
RUN pacman -Syu --noconfirm
RUN pacman -S base-devel --noconfirm
RUN pacman -S vi vim --noconfirm
RUN pacman -S tmux --noconfirm
RUN pacman -S git --noconfirm
RUN pacman -S wget --noconfirm
RUN pacman -S cmake --noconfirm
RUN pacman -S gdb --noconfirm
RUN pacman -S zsh --noconfirm
RUN pacman -S zsh-theme-powerlevel10k --noconfirm
RUN pacman -S zsh-syntax-highlighting --noconfirm
RUN pacman -S zsh-autosuggestions --noconfirm
RUN pacman -S zsh-completions --noconfirm
RUN pacman -S zoxide --noconfirm
RUN pacman -S fzf --noconfirm
RUN pacman -S unzip --noconfirm
# add archlinuxcn and yay
RUN echo '[archlinuxcn]' >> /etc/pacman.conf
RUN echo 'Server = https://mirrors.tuna.tsinghua.edu.cn/archlinuxcn/$arch' >> /etc/pacman.conf
RUN pacman -Sy archlinuxcn-keyring --noconfirm
RUN rm -R /etc/pacman.d/gnupg
RUN pacman-key --init
RUN pacman-key --populate archlinux
RUN pacman-key --populate archlinuxcn
RUN pacman -S yay --noconfirm
# use config
RUN sed -i 's/# %wheel ALL=(ALL:ALL) ALL/%wheel ALL=(ALL:ALL) ALL/' /etc/sudoers
RUN useradd -m -s /bin/zsh jxm2001
RUN usermod -aG wheel jxm2001
RUN echo jxm2001:jxm2001 | chpasswd
USER jxm2001
WORKDIR /home/jxm2001
COPY --chown=jxm2001:jxm2001 ./zshrc /home/jxm2001/.zshrc
CMD /bin/zsh