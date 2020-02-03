FROM amd64/ubuntu
RUN apt-get update
RUN apt-get --yes install cbmc
RUN apt-get --yes install clang
RUN apt-get --yes install apt-utils
RUN apt-get --yes install python3-dev libffi-dev build-essential virtualenvwrapper
RUN apt-get --yes install python3-pip
RUN useradd -m  static
WORKDIR /home/static
USER static
RUN mkdir .virtualenv
RUN virtualenv -p /usr/bin/python3 /home/static/.virtualenv/angr
RUN . /home/static/.virtualenv/angr/bin/activate && pip3 install angr
