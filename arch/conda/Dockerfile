FROM jxm2001/arch:zsh
USER root
WORKDIR /root
RUN pacman -S python-pip --noconfirm
RUN pacman -S miniconda --noconfirm
USER jxm2001
WORKDIR /home/jxm2001
RUN pip config set global.index-url https://pypi.tuna.tsinghua.edu.cn/simple
RUN source /opt/miniconda/etc/profile.d/conda.sh && conda init zsh
CMD /bin/zsh
