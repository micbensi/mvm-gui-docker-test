FROM debian:10.3
ENV LANG en_US.UTF8
ENV LANGUAGE en_US:en
ENV LC_ALL en_US.UTF-8
RUN echo "deb http://deb.debian.org/debian sid main contrib" >> \
    /etc/apt/sources.list.d/unstable.list && apt-get update && \
    apt-get -y install locales-all locales python3 \
    python3-pyqt5 python3-pyqtgraph python3-numpy python3-serial \
    python3-pytest python3-pytestqt python3-coverage \
    python3-pytest-xvfb python3-xvfbwrapper && \
    apt-get -t sid -y install python3-yaml && \
    apt-get clean && \
    groupadd -g 1000 pi && useradd -u 1000 -g 1000 -m -s /bin/bash pi && \
    ln -s /usr/bin/pytest-3 /usr/bin/pytest && \
    ln -s /usr/bin/python3 /usr/bin/python
USER pi
