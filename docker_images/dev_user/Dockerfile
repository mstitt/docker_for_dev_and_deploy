
FROM ubuntu:14.04

RUN apt-get update && apt-get install --yes wget build-essential zile

RUN groupadd --gid 1000 ziggy
RUN useradd --uid 1000 --gid 1000 --create-home --shell /bin/bash ziggy
RUN echo "ziggy ALL=(ALL) NOPASSWD:ALL" >> /etc/sudoers

USER ziggy

ENV HOME /home/ziggy
WORKDIR /home/ziggy/
CMD /bin/bash
