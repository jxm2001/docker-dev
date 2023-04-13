FROM jxm2001/ubuntu:base
USER jxm2001
WORKDIR /home/jxm2001
RUN mkdir -p ~/.zsh/theme
RUN mkdir -p ~/.zsh/plugins
COPY --chown=jxm2001:jxm2001 ./plugins/powerlevel10k /home/jxm2001/.zsh/themes/powerlevel10k
COPY --chown=jxm2001:jxm2001 ./plugins/zsh-syntax-highlighting /home/jxm2001/.zsh/plugins/zsh-syntax-highlighting
COPY --chown=jxm2001:jxm2001 ./plugins/zsh-autosuggestions /home/jxm2001/.zsh/plugins/zsh-autosuggestions
COPY --chown=jxm2001:jxm2001 ./plugins/zsh-completions /home/jxm2001/.zsh/plugins/zsh-completions
COPY --chown=jxm2001:jxm2001 ./plugins/z /home/jxm2001/.zsh/plugins/z
COPY --chown=jxm2001:jxm2001 ./plugins/fzf /home/jxm2001/.zsh/plugins/fzf
COPY --chown=jxm2001:jxm2001 ./zshrc /home/jxm2001/.zshrc
CMD /bin/zsh

