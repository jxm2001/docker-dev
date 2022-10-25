FROM ubuntu
RUN sed -ri.bak -e 's/\/\/.*?(archive.ubuntu.com|mirrors.*?)\/ubuntu/\/\/mirrors.pku.edu.cn\/ubuntu/g' -e '/security.ubuntu.com\/ubuntu/d' /etc/apt/sources.list
RUN apt update
RUN apt upgrade -y
RUN apt install build-essential -y
RUN apt install vim -y
RUN apt install tmux -y
RUN apt install git -y
RUN apt install curl -y
RUN apt install wget -y
RUN apt install cmake -y
RUN apt install gdb -y
RUN apt install zsh -y
RUN apt install fzf -y
RUN apt install sudo -y
RUN useradd -m -s /bin/zsh jxm2001
RUN usermod -aG sudo jxm2001
RUN echo jxm2001:jxm2001 | chpasswd
