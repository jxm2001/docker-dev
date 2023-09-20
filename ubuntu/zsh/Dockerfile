FROM jxm2001/ubuntu:base
RUN chsh -s /usr/bin/zsh
RUN mkdir -p /root/.zsh/theme
RUN mkdir -p /root/.zsh/plugins
COPY ./plugins/powerlevel10k /root/.zsh/themes/powerlevel10k
COPY ./plugins/zsh-syntax-highlighting /root/.zsh/plugins/zsh-syntax-highlighting
COPY ./plugins/zsh-autosuggestions /root/.zsh/plugins/zsh-autosuggestions
COPY ./plugins/zsh-completions /root/.zsh/plugins/zsh-completions
COPY ./plugins/z /root/.zsh/plugins/z
COPY ./plugins/fzf /root/.zsh/plugins/fzf
COPY ./zshrc /root/.zshrc
WORKDIR /root
CMD /bin/zsh
