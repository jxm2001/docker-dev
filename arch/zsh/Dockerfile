FROM jxm2001/arch:base
# base build
USER root
WORKDIR /root
RUN pacman -S zsh-theme-powerlevel10k --noconfirm
RUN pacman -S zsh-syntax-highlighting --noconfirm
RUN pacman -S zsh-autosuggestions --noconfirm
RUN pacman -S zsh-completions --noconfirm
RUN pacman -S zoxide --noconfirm
RUN pacman -S fzf --noconfirm
USER jxm2001
WORKDIR /home/jxm2001
COPY --chown=jxm2001:jxm2001 ./zshrc /home/jxm2001/.zshrc
CMD /bin/zsh
