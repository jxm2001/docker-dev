FROM jxm2001/ubuntu:ssh
RUN wget -O miniconda3.sh https://repo.anaconda.com/miniconda/Miniconda3-latest-Linux-x86_64.sh
RUN /bin/bash miniconda3.sh -b
RUN /bin/bash -c "source /root/miniconda3/etc/profile.d/conda.sh && conda init zsh"
RUN rm miniconda3.sh
