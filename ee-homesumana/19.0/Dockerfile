FROM odoo:19
ENV TZ=Asia/Bangkok

USER root

RUN apt-get update \
    && locale -a \
    && apt -y install vim-tiny procps htop iputils-ping \
    && apt -y install net-tools wget lynx unzip rsync iw

RUN apt-get update \
    && apt-get -y install git curl gcc libpython3-dev \
    && apt-get -y install rustc

RUN apt-get update \
    && apt-get -yq install locales tzdata fonts-tlwg-laksaman \
    && sed -i 's/# th_/th_/' /etc/locale.gen \
    && locale-gen \
    && cp /usr/share/zoneinfo/Asia/Bangkok /etc/localtime \
    && echo "Asia/Bangkok" > /etc/timezone \
    && dpkg-reconfigure -f noninteractive tzdata

RUN echo "alias v='ls -al'" >> /etc/bash.bashrc

USER odoo
