ARG BASE_IMAGE
FROM ${BASE_IMAGE}

ENV container=docker

RUN if command -v pacman > /dev/null; then \
      pacman --sync --refresh --noconfirm systemd systemd-sysvcompat python; \
    elif command -v apt-get > /dev/null; then \
      apt-get update && \
      DEBIAN_FRONTEND=noninteractive apt-get install --yes systemd systemd-sysv python3 python3-apt; \
    else \
      dnf install --assumeyes systemd python3 python3-libdnf5 && \
      dnf clean all; \
    fi

STOPSIGNAL SIGRTMIN+3
CMD ["/sbin/init"]