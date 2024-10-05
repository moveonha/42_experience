FROM debian:buster-slim
RUN apt-get update \
    && apt-get install -y dumb-init curl git python3 python3-venv build-essential python3-pip clang vim libbsd-dev valgrind \
    && python3 -m pip install --upgrade pip setuptools \
    && python3 -m pip install norminette
RUN bash -c "$(curl -fsSL https://raw.github.com/xicodomingues/francinette/master/bin/install.sh)"
ENTRYPOINT ["/usr/bin/dumb-init", "--"]
CMD ["bash"]
