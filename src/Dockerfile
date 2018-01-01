FROM tianon/steam

RUN sudo apt update && \
    sudo apt install gdb -y

USER steam
ENV HOME /home/steam
VOLUME /home/steam

CMD ["steam"]
