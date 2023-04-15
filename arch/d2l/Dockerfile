FROM jxm2001/arch:conda
RUN /bin/bash -c "source /opt/miniconda/etc/profile.d/conda.sh \
    && conda create --name d2l python=3.9 -y"
RUN /bin/bash -c "source /opt/miniconda/etc/profile.d/conda.sh \
    && conda activate d2l \
	&& pip install torch==1.12.0 \
	&& pip install torchvision==0.13.0"
RUN /bin/bash -c "source /opt/miniconda/etc/profile.d/conda.sh \
    && conda activate d2l \
	&& pip install d2l==0.17.6"
RUN curl https://zh-v2.d2l.ai/d2l-zh-2.0.0.zip -o d2l-zh.zip
RUN unzip d2l-zh.zip
WORKDIR /home/jxm2001/pytorch
CMD /bin/zsh
